# Gor-PathologyAssignment--Script

import java.time.Duration;

import org.openqa.selenium.By;
import org.openqa.selenium.JavascriptExecutor;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.support.ui.ExpectedConditions;
import org.openqa.selenium.support.ui.Select;
import org.openqa.selenium.support.ui.WebDriverWait;

public class gor {

	public static void main(String[] args) throws InterruptedException {

		WebDriver driver = new ChromeDriver();
		
		//Login page and home page
		
		driver.get("https://gor-pathology.web.app/patients/add");

		Thread.sleep(5000);
		
		driver.manage().window().maximize();
		
		driver.findElement(By.xpath("//input[@name='email']")).sendKeys("test@kennect.io");
		
		driver.findElement(By.xpath("//input[@name='password']")).sendKeys(("Qwerty@1234"));
		
		driver.findElement(By.xpath("//span[normalize-space()='Login']")).click();
		
		
		Thread.sleep(5000);
		//  Cost Calculator for Blood Test
		
		driver.findElement(By.xpath("//span[normalize-space()='Dashboard']")).click();
		
		Thread.sleep(5000);
		
		((JavascriptExecutor) driver).executeScript("window.scrollBy(0, 500);");
		
		
		Thread.sleep(5000);

		WebElement dropdown = driver.findElement(By.xpath("//*[@id='patient-test']"));
        dropdown.click();
        Thread.sleep(1000);

        // Click on the first option's checkbox
        WebElement firstCheckbox = driver.findElement(By.xpath("//li[@id='patient-test-option-1']//input[@type='checkbox']"));
        firstCheckbox.click();
        Thread.sleep(2000);

		// Click the first option

        // Step 4: Second dropdown - open discount menu
        WebElement discountDropdown = driver.findElement(By.xpath("//*[@id='root']/div/main/div[2]/div[3]/div/div[2]/div[2]/div/div"));
        discountDropdown.click();
        Thread.sleep(3000);

        // Step 5: Click the '10%' discount option
        WebElement discountOption = driver.findElement(By.xpath("//*[@id=\"menu-\"]/div[3]/ul/li[2]"));
        discountOption.click();
        Thread.sleep(2000);
        
     // Step 6: Click on "Patients" menu
        WebElement patientsMenu = driver.findElement(By.xpath("//span[normalize-space()='Patients']"));
        patientsMenu.click();
        Thread.sleep(2000);
        
        
     // Step 7: Click on "Add Patient" button
        WebElement addPatientBtn = driver.findElement(By.xpath("//*[@id='root']/div/main/div[2]/div[1]/a/button/span[1]"));
        addPatientBtn.click();
        Thread.sleep(2000);

        
     // Step 8: Enter patient name
        WebElement nameInput = driver.findElement(By.xpath("//input[@name='name']"));
        nameInput.sendKeys("Yogesh");
        Thread.sleep(1000);

        // Step 9: Enter patient email
        WebElement emailInput = driver.findElement(By.xpath("//input[@name='email']"));
        emailInput.sendKeys("shingne.yogesh@gmail.com");
        Thread.sleep(1000);

        // Step 10: Enter patient phone number
        WebElement phoneInput = driver.findElement(By.xpath("//input[@name='phone']"));
        phoneInput.sendKeys("7875188566");
        Thread.sleep(1000);

        // Step 11: Click "Generate Details" button
        WebElement generateDetailsBtn = driver.findElement(By.xpath("//*[@id=\"root\"]/div/main/div[2]/div[2]/div/div[2]/div[2]/button[2]/span[1]"));
        generateDetailsBtn.click();
        Thread.sleep(2000);

     // Step 12: Enter height (in cm)
        WebElement heightInput = driver.findElement(By.xpath("//input[@name='height']"));
        heightInput.sendKeys("170");
        Thread.sleep(1000);

        // Step 13: Enter weight (in kg)
        WebElement weightInput = driver.findElement(By.xpath("//input[@name='weight']"));
        weightInput.sendKeys("75");
        Thread.sleep(1000);

        // Step 14: Select gender (Male)
        WebElement genderDropdown = driver.findElement(By.xpath("//div[@id='mui-component-select-gender']"));
        genderDropdown.click();
        Thread.sleep(1000);

        // Select first option (Male) from dropdown
        WebElement maleOption = driver.findElement(By.xpath("//li[normalize-space()='Male']"));
        maleOption.click();
        Thread.sleep(1000);

        // Step 15: Enter age
        WebElement ageInput = driver.findElement(By.xpath("//input[@name='age']"));
        ageInput.sendKeys("30");
        Thread.sleep(1000);

        
		
		((JavascriptExecutor) driver).executeScript("window.scrollBy(0, 500);");
		
		Thread.sleep(2000);

		
        // Step 16: Enter systolic
        WebElement systolicInput = driver.findElement(By.xpath("//input[@name='systolic']"));
        systolicInput.sendKeys("80");
        Thread.sleep(1000);

        // Step 17: Enter diastolic
        WebElement diastolicInput = driver.findElement(By.xpath("//input[@name='diastolic']"));
        diastolicInput.sendKeys("90");
        Thread.sleep(1000);

        // Step 18: Click "Add Test" button
     // Step 18: Click "Add Test" button (robust locator)
        WebElement addTestButton = driver.findElement(By.xpath("//button[.//span[contains(text(),'Add Test')]]"));
        addTestButton.click();
        Thread.sleep(5000);


		
        JavascriptExecutor js = (JavascriptExecutor) driver;
        js.executeScript("window.scrollTo(0, 0);");
		
        driver.findElement(By.xpath("//*[@id='patient-test']")).click();
        
        Thread.sleep(5000);

        
     // Click the first checkbox option after the dropdown or list appears
        WebElement firstOptionCheckbox = driver.findElement(By.xpath("//*[@id='patient-test-option-1']//input[@type='checkbox']"));
        firstOptionCheckbox.click(); // This clicks the first option inside the dropdown or list
        Thread.sleep(5000); // W
        
      driver.findElement(By.xpath("//*[@id=\"root\"]/div/main/div[2]/div[2]/div/div[1]/div[1]/div[2]/div[2]/div/div")).click();
       Thread.sleep(5000);

         WebElement checkbox = driver.findElement(By.xpath("//ul[@role='listbox']/li[1]"));
         checkbox.click();         
		((JavascriptExecutor) driver).executeScript("window.scrollBy(0, 500);");

		
		
	}

}
