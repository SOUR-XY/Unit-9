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
