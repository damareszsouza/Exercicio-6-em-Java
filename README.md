# Exercicio-6-em-Java

# Exercicio replicado do livro Tutorial de Programação em Java e Orientação em Objetos

# Programa exemplo círculo, baseado no exemplo de ATRIBUTOS:

//Classe circulo
public class Circulo {
public float raio,x,y;
public void inicializa(float ax,float ay,float ar)
//garante o estado do objeto
{
 this.x = ax; this.y = ay; this.raio = ar;
}
public void setRaio(float a)
{
 this.raio = a;
}
public float getRaio()
{
 return this.raio;
}
public void move(float dx,float dy) {
 this.x += dx; this.y += dy;
}
public void mostra()
{
 System.out.println("(" + this.x + "," + this.y + "," + this.getRaio()+")");
}
}
//Classe principal, Arquivo Principal.Java
public class Principal {
 public static void main(String args[]) {
 Circulo ac;
 ac = new Circulo();
 ac.inicializa(0,0,10);
 ac.mostra();
 ac.move(1,1);
 ac.mostra();
 ac.x = 100;
 ac.setRaio(12);
 ac.mostra();
 
 }
 }
 
 //Observe que o método mostra chama o método public float getRaio() que é da mesma classe.
//Fica claro da definição de mostra que this.getRaio() se aplica ao mesmo objeto instanciado que
//recebeu a chamada de mostra. Isto foi feito somente para revelar que chamadas aninhadas de
//métodos também são permitidas, pois nesse caso esta chamada de método poderia ser substituída pelo
//próprio atributo raio, o que seria mais eficiente.
