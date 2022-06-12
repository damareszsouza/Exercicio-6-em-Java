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

# Pascal: Um programa parecido só que em Pascal:

 PROGRAM Comparacao;

{COMPARACAO COM UM PROGRAMA Java}
TYPE Circulo=RECORD
 x:real;
 {COORDENADAS X E Y}
 y:real;
 r:real;
 {somente dados}
 END;
var ac:circulo;
 leitura:integer;
PROCEDURE Inicializa(var altereme:Circulo;ax,by,cr:real);
 {COLOCA O CIRCULO EM DETERMINADA POSICAO}
BEGIN
 altereme.x:=ax;
 altereme.y:=by;
 altereme.r:=cr;
END;
PROCEDURE Altera_Raio(var altereme:Circulo;ar:real);
{ALTERA O RAIO DO CIRCULO}
BEGIN
 altereme.r:=ar;
END;
FUNCTION Retorna_Raio(copieme:Circulo):real;
BEGIN
 Retorna_Raio:=copieme.r;
END;
PROCEDURE Move(var altereme:Circulo;dx,dy:real);
{MODE AS COORDENADAS X E Y ACRESCENTANDO DX E DY}
BEGIN
 altereme.x:=altereme.x+dx;
 altereme.y:=altereme.y+dy;
END;
PROCEDURE Mostra(copieme:Circulo);
{MOSTRA O CIRCULO NA TELA}
BEGIN
 writeln('X:',copieme.x,' Y:',copieme.y,' R:',copieme.r);
END;
BEGIN
{TESTES}
 Inicializa(ac,0.0,0.0,10.0);
 Mostra(ac);
 Move(ac,1.0,1.0);
 Mostra(ac);
 ac.x:=100.0;
 Altera_Raio(ac,12.0);
 Mostra(ac);
 read(leitura);
 END.
 
 //COMENTARIOS JAVA:
As classes em Java são compostas de atributos e métodos. Para executar uma ação sobre o
objeto ou relativa a este basta chamar um método : ac.mostra(); O método não precisa de muitos
argumentos, porque é próprio da classe e portanto ganha acesso aos atributos do objeto para ao qual
ela foi associado:
public float getRaio(void)
{ return raio; //tenho acesso direto a raio. }
{ COMEntArios Pascal: }
Em Pascal os procedimentos e os dados são criados de forma separada, mesmo que só tenham
sentido juntos. A junção entre os dados e procedimentos se dá através de passagem de parâmetros. No
caso de uma linguagem procedural, o que normalmente é feito se assemelha ao código seguinte:
Move(ac, 1.0,1.0);. Nesse caso AC é um “record”, algo semelhante ao struct de C (não C++).
Move, acessa os dados do “record” alterando os campos. O parâmetro é passado por referência e o
procedimento é definido a parte do registro, embora só sirva para aceitar argumentos do tipo Circulo
e mover suas coordenadas.

