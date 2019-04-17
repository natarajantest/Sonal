package package1;

import java.util.concurrent.TimeUnit;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.interactions.Actions;
import org.openqa.selenium.support.ui.Select;

public class AddPatient {

	public static void main(String[] args) throws InterruptedException {
		// TODO Auto-generated method stub
		WebDriver driver = new ChromeDriver();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(30, TimeUnit.SECONDS);
		driver.get("https://demo.openemr.io/d/openemr");
		driver.findElement(By.className("form-control")).sendKeys("admin");
		driver.findElement(By.id("clearPass")).sendKeys("pass");
		driver.findElement(By.xpath("//i[@class='fa fa-sign-in']")).click();
		Actions act=new Actions(driver);
		act.moveToElement(driver.findElement(By.xpath("//div[text()='Patient/Client']"))).build().perform();
		act.click(driver.findElement(By.xpath("//div[text()='New/Search']"))).build().perform();
		driver.switchTo().frame(driver.findElement(By.xpath("//iframe[@name='pat']")));
		driver.findElement(By.id("form_fname")).sendKeys("Sonal");
		driver.findElement(By.id("form_lname")).sendKeys("Gorivale");
		driver.findElement(By.id("form_DOB")).sendKeys("17-04-2019");
		//act.click(driver.findElement(By.partialLinkText("17"))).build().perform();
		Select gender=new Select(driver.findElement(By.id("form_sex")));
		gender.selectByValue("Female");
		driver.findElement(By.id("create")).click();
		driver.switchTo().defaultContent();
		   
	    driver.switchTo().frame(driver.findElement(By.xpath("//iframe[@class='embed-responsive-item modalIframe']")));
	    driver.findElement(By.xpath("//input[@value='Confirm Create New Patient']")).click();
	    Thread.sleep(3000);
	    driver.switchTo().alert().accept();
	    
	   
	    
	    driver.findElement(By.xpath("//div[@class='closeDlgIframe']")).click();
	   // driver.switchTo().frame(driver.findElement(By.name("timeout")));
	   // Actions act1=new Actions(driver);
	    act.moveToElement(driver.findElement(By.xpath("//div[@class='menuSection userSection']"))).build().perform();
	    driver.findElement(By.xpath("//ul//li[text()='Logout']")).click();


	}

}
