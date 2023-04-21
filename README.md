# 202001419_Lab8

SOFTWARE ENGINEERING 

Name - Rushabh Patel (202001419)

1) Create a new Eclipse project, and within the project create a package.
<img width="238" alt="image" src="https://user-images.githubusercontent.com/77353523/233616360-0381da9c-2400-4408-ac60-7f455ecf0803.png">
<img width="960" alt="image" src="https://user-images.githubusercontent.com/77353523/233616440-88c86f1b-ca92-4247-8164-d606e6fe61f5.png">


package tests;

public class Boa {
	private String name;
	private int length; // the length of the boa, in feet
	private String favoriteFood;
	
	public Boa (String name, int length, String favoriteFood){
		this.name = name;
		this.length = length;
		this.favoriteFood = favoriteFood;
	}
	
	// returns true if this boa constrictor is healthy
	public boolean isHealthy(){
		return this.favoriteFood.equals("granola bars");
	}
	
	// returns true if the length of this boa constrictor is
	// less than the given cage length
	public boolean fitsInCage(int cageLength){
		return this.length < cageLength;
	}
}
<img width="960" alt="image" src="https://user-images.githubusercontent.com/77353523/233616657-e886560f-cc23-4621-90b9-7ad860646054.png">


package tests;

import org.junit.Before;
import static org.junit.Assert.*;
import org.junit.Test;

public class BoaTest {
	private Boa jen;
	private Boa ken;

	@Before
	public void setUp() throws Exception {
	jen = new Boa("Jennifer", 2, "grapes");
	ken = new Boa("Kenneth", 3, "granola bars"); }
	
	/*@Test
	public void testBoa() {
		fail("Not yet implemented");
	}*/

	@Test
	public void testIsHealthy() {
		assertEquals(false, jen.isHealthy()); assertEquals(true, ken.isHealthy());
	}

	@Test
	public void testFitsInCage() {
		assertEquals(false , jen.fitsInCage(1)); assertEquals(true , ken.fitsInCage(5));
	}

}
<img width="960" alt="image" src="https://user-images.githubusercontent.com/77353523/233617091-0d8ec290-583c-494b-bd8a-16cb9bdd7965.png">


Code for LengthInInches

public int lengthInInches(){

// you need to write the body of this method int length_to_Inches;

length_to_Inches= 12 * this.length;

return length_to_Inches;

}

Test for lengthinInInches

@Test

public void testlengthInInches() { assertEquals(24,jen.lengthInInches());

assertEquals(12,ken.lengthInInches());
