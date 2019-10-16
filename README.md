# Unit-9

9-1
public class text {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
       SimpleCircle circle1 = new SimpleCircle();
       System.out.println("The area of the circle of radius" + circle1.radius + " is " + 
       circle1.getArea());
       
       SimpleCircle circle2 = new SimpleCircle(25);
       System.out.println("The area of the circle of radius" + circle2.radius + " is " + 
       circle1.getArea()); 
       
       SimpleCircle circle3 = new SimpleCircle(125);
       System.out.println("The area of the circle of radius" + circle3.radius + " is " + 
       circle1.getArea());
       
       circle2.setRadius(100);
       System.out.println("The area of the circle of radius" + circle2.radius + " is " + 
       circle1.getArea());
	}
}

class SimpleCircle{
	double radius;
	
	SimpleCircle(){
		radius = 1;
	}
	
	SimpleCircle(double newRadius){
		radius = newRadius;
	}
	
	double getArea(){
		return radius * radius * Math.PI;
	}
	
	double getPrimeter(){
		return 2 * radius * Math.PI;
	}
	
	void setRadius(double newRadius){
		radius = newRadius;
	}
}

9-2
public class SimpleCircle {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
       SimpleCircle circle1 = new SimpleCircle();
       System.out.println("The area of the circle of radius" + circle1.radius + " is " + 
       circle1.getArea());
       
       SimpleCircle circle2 = new SimpleCircle(25);
       System.out.println("The area of the circle of radius" + circle2.radius + " is " + 
       circle1.getArea()); 
       
       SimpleCircle circle3 = new SimpleCircle(125);
       System.out.println("The area of the circle of radius" + circle3.radius + " is " + 
       circle1.getArea());
       
       circle2.setRadius(100);
       System.out.println("The area of the circle of radius" + circle2.radius + " is " + 
       circle1.getArea());
	}
}

	double radius;
	
	SimpleCircle(){
		radius = 1;
	}
	
	SimpleCircle(double newRadius){
		radius = newRadius;
	}
	
	double getArea(){
		return radius * radius * Math.PI;
	}
	
	double getPrimeter(){
		return 2 * radius * Math.PI;
	}
	
	void setRadius(double newRadius){
		radius = newRadius;
	}
}

9-3
public class TV {
	int channel = 1;
	int volumeLevel = 1;
	boolean on = false;

	public TV(){
	}
	public void turnon(){
		on = true;
	}
	public void turnoff(){
		on = false;
	}
	public void setchannel(int newChannel){
		if(on && newChannel >= 1 && newChannel <= 120)
			channel = newChannel;
	}
	public void setvolume(int newVolumeLevel){
		if(on && newVolumeLevel >= 1 && newVolumeLevel <= 7)
			volumeLevel = newVolumeLevel;
	}
	public void channeldown(){
		if(on && channel > 1)
			channel--;
	}
	public void channelup(){
		if(on && channel < 120)
			channel++;
	}
	public void volumedown(){
		if(on && volumeLevel > 1)
			volumeLevel--;
	}
	public void volumedown(){
		if(on && volumeLevel < 7)
			volumeLevel++;
	}
	
}

9-4
public class testtv {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		TV tvl = new TV();
		tvl.turnon();
		tvl.setchannel(30);
		tvl.setvolume(3);
		
		TV tv2 = new TV();
		tv2.turnon();
		tv2.channelup();
		tv2.channelup();
		tv2.volumeup();
		
		System.out.println("tvl channel is" + tvl.channel + "and volume level is" +
		tvl.channel + "and volume level is " + tvl.volumelevel);
		System.out.println("tv2 channel is" + tv2.channel + "and volume level is" +
				tv2.channel + "and volume level is " + tv2.volumelevel);
	}
}

9-5
import java.util.Scanner;
import javafx.geometry.Point2D;
public class TestPoint2D {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
        Scanner input = new Scanner(System.in);
        
        System.out.print("enter point1  x-,y-coordinates: ");
        double x1 = input.nextDouble();
        double y1 = input.nextDouble();
        System.out.print("enter point2  x-,y-coordinates: ");
        double x2 = input.nextDouble();
        double y2 = input.nextDouble();
        
        Point2D p1 = new Point2D(x1,y1);
        Point2D p2 = new Point2D(x2,y2);
        System.out.println("p1 is " + p1.toString());
        System.out.println("p2 is " + p2.toString());
        System.out.println("the distance between p1 and p2 is" + p1.distance(p2));
	}
}

9-6
public class helloo {
	double radius;
	static int numberofobjects = 0;
	
	circlewithstaticmember(){
		radius = 1;
		numberofobjects++;
	}
	
	circlewithstaticmembers(double newradius){
		radius = newradius;
		numberofobjects++;
	}
	
	static int getnumberofobjects() {
		return numberofobjects;
	}
	
	double getarea() {
		return radius *radius *Math.PI;
	}
}

9-7
public class tess {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
       System.out.println("before creating objects");
       System.out.println("the number of circle objects is"+
       circlewithstaticmembers.numberofobjects);
       
       cieclewithstaticmembers c1 = new circlewithstaticmembers();
       
       System.out.println("\nafter creating c1");
       System.out.println("c1:radius("+c1.radius+") and number of circle objects(" + c1.numberofobjects
    		   +")");
       
       circlewithstaticmembers c2 = new circlewithstaticmember(5);
       
       c1.radius=9;
       System.out.printfln("\nafter creating c2 and modifying c1");
       System.out.printfln("c1:radius (" + c1.radius+") and number of circle objects ("+
       c1.numberofobjects+")");
       System.out.printfln("c2:radius (" + c2.radius+") and number of circle objects ("+
       c2.numberofobjects+")");
	}

}

9-8
public class tsst {
	private double radius =1;
	private static int numberofobjects=0;
	
	public circlewithprivatedatafields() {
		numberofobjects++;
	}
	
	public circlewithprivatedatafields(double newradius) {
		radius = newradius;
		numberofobjects++;
	}
	
	public double getradius() {
		return radius;
	}
	
	public void setradius(double newradius) {
		radius=(newradius>=0)?newradius:0;
	}
	
	public static int getnumberofobjects() {
		return numberofobjects;
	}
	
	public static int getnumberofobjects() {
		return numberofobjects;
	}
	
	public double getarea() {
		return radius *radius *Math.PI;
	}

}

9-9
public class tess {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
        circlewithprivatedatafields mycircle=
        		new circlewithprivatedatafields(5.0);
        System.out.printfln("the area of the circle of radius"+
        		mycircle.getradius()+"is"+mycircle.getarea());
        
        mycircle.setradius(mycircle.getradius()*1.1);
        System.out.println("the area of the radius" + mycircle.getradius()+" is "+ 
        mycircle.getarea());
        
        System.out.println("the number of objects created is "+
        cieclewithprivatedatafields.getnumberofobjects());
	}
}

9-10
public class tess {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
        circlewithprivatedatafields mycircle =
        		new circlewithprivatedatafields(1);
        
        int n=5;
        printareas(mycircle,n);
        
        System.out.println("\n" + "Radius is" +mycircle.getradius());
        System.out.println("n is" + n);
        
        public static void printareas(
        		circlewithprivatedatafields c,int times) {
        	System.out.println("radius\t\tarea");
        	while(times>=1)
        	{
        		System.out.println(c.getradius()+"\t\t"+c.getarea());
        		c.setradius(c.getradius()+1);
        		times--;
        	}
        }
	}
}

9-11
public class tess {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
        circlewithprivatedatafields[] circlearray;
        
        circlearray(circlearray);
        
        public static circlewithprivatedatafields[] createcirclearray() {
        	circlewithprivatedatafields[] circlearray =
        			new circlewithprivatedatafields[5];
        	
        	for(int i=0;i<circlearray.length;i++)
        	{
        		circlearray[i]=
        				new circlewithprivatedatafields(Math.random()*100);
        	}
        	return circlearray;
        }
        public static void printcirclearray(
        		circlewithprivatedatafields[] circlearray) {
        	System.out.printf("%-30s%-15s\n", "radius","area");
        	for(int i=0;i<circlearray.length;i++)
        	{
        		System.out.printf("%-30f%-15f\n",circlearray[i].getradius(),
        				circlearray[i].getarea());
        	}
        	System.out.printf("%-30s%-15f\n", "the total area of circles is",
        			sum(circlearray));
        }
        public statics double sum(circlewithprivatedatafields[] circlearray) {
        	double sum = 0;
        	for(int i=0;i<circlearray.length;i++)
        		sum+=circlearray[i].getarea();
        	return sum;
        }
        	
        
	}
}
