
public class Car {

	private String model; // model of the car
	private String color; // color of the car
	private int year; // year of the car
	private int fMiles; // miles from the beginning  
	private int gallons; // gallons filled for construction 
	private double price; // total cost of gallons
	private double mpg; // average of miles over entire life
	
	public Car(String mdl, String clr, int yr) 
	{
		model = mdl;
		color = clr;
		year = yr;
		fMiles = 0;
		gallons = 0;
		price = 0;
	}
	
	public Car(String mdl, String clr, int y, int mls, int gls, double pr) 
	{
		model = mdl;
		color = clr; 
		year = y;
		fMiles = mls; 
		gallons = gls;
		price = pr;
	}
	
	public int getMiles() 
	{
		return fMiles;
	}
	
	public int getGallons() 
	{
		return gallons; 
	}
	
	public double getFuelCost()
	{
		return price;
	}
	
	public double getPrice() 
	{
		return price; 
	}
	
	public String getModel()
	{
		return model; 
	}
	
	public String getColor()
	{
		return color; 
	}
	
	public int getYear()
	{
		return year;
	}
	
	public void fillup(int addedGls, int addedMls, double totalP) 
	{	
		gallons = gallons + addedGls;
		fMiles = fMiles + addedMls;
		price = price + totalP;	
	}
	
	public double getMPG()
	{
		if(gallons==0) 
		{
			return 0;
		}
		else {
			mpg = (double)fMiles/gallons;
			return mpg;
			}
		
	}
	
	public String toString()
	{
		return year + " " + color + " " + model + " " + fMiles + " miles";
	}
	


}
