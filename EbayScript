# EbayScript
package testCases;
import java.io.File; 
import java.net.MalformedURLException;
import java.net.URL;
import java.util.List;
import java.util.Random;
import java.util.concurrent.TimeUnit;

import org.openqa.selenium.remote.DesiredCapabilities;
import org.testng.annotations.AfterMethod;
import org.testng.annotations.AfterTest;
import org.testng.annotations.BeforeMethod;
import org.testng.annotations.BeforeTest;
import org.testng.annotations.Test;

import io.appium.java_client.MobileElement;
import io.appium.java_client.TouchAction;
import io.appium.java_client.android.AndroidDriver;
import io.appium.java_client.android.AndroidElement;
import io.appium.java_client.android.AndroidKeyCode;
import objectrepository.EbayLogin;

@Test
public class EbayScript {
	public static AndroidDriver<MobileElement> driver; 
	 
	public void EbayTest() throws InterruptedException {
		 EbayLogin Ebay=new EbayLogin(driver);
			
			Ebay.Sign().click();
			Ebay.Edit().click();
			Ebay.Edit().clear();;
			Ebay.Edit().sendKeys("diwakartesting@gmail.com");
			Ebay.Pwd().click();
			Ebay.Pwd().clear();;
			Ebay.Pwd().sendKeys("Diwa@1056");
			Ebay.Signin().click();
			Thread.sleep(3000);
			Ebay.Maybe().click();
			Thread.sleep(5000);
			
			Ebay.search().click();
			Ebay.Serc().clear();
			Ebay.Serc().sendKeys("samsung 65 led tv");
			Thread.sleep(3000); 
			driver.pressKeyCode(AndroidKeyCode.KEYCODE_ENTER);
			Thread.sleep(6000);
			TouchAction action = new TouchAction(driver);
			int startX = 606;
			int startY=610;
			int endX=620;
			int endY=622;
			action.press(startX, startY).moveTo((endX - startX), (endY-

startY)).release().perform();
			Thread.sleep(6000);
			
			List<MobileElement> elementList = 

driver.findElementsByClassName("android.widget.RelativeLayout");
			System.out.println("Total elements : " + elementList.size());
			Thread.sleep(2000);
			Random rand = new Random();
			int index = rand.nextInt(elementList.size()); 
			elementList.get(index).click();
			Thread.sleep(5000);
			String cc=Ebay.Text().getText().trim();
	        System.out.println(cc);
			String ee=Ebay.Pric().getText().trim();
	                System.out.println(ee);
	                Thread.sleep(5000);
					Ebay.Buy().click();
	                Thread.sleep(4000);
					Ebay.Rew().click();
					Thread.sleep(10000);
					action.press(startX, startY).moveTo((endX - 

startX), (endY-startY)).release().perform();
	                Thread.sleep(3000);
	                            System.out.println(cc);
				String Namever=driver.findElementByXPath("//*[@text='" 

+ cc + "']").getText().trim();
	            System.out.println(Namever);
	            if (cc.equals(Namever)) {
	                System.out.println("Text Name is passed ");
	            } else {
	              System.out.println("Text Name is failed.");
	            }
	           
	           String rr= driver.findElementByXPath

("//android.webkit.WebView/android.view.View/android.view.View[3]/android.view.View

[4]/android.view.View[2]/android.view.View[2]/android.view.View

[2]/android.view.View/android.view.View[3]").getText().trim();
	           String bodyText = driver.findElementByXPath("//*[@text='" + rr + 

"']").getText().trim();
	           System.out.println(bodyText);
	           if (rr.equals(bodyText)) {
	                System.out.println("Price is Matched");
	           } else {
	              System.out.println("Price is Mismatched.");
	           }
	           System.out.println( bodyText );
	              	         	   
	        	  
				
	 }
	

	
	
	
	
@BeforeTest
	public void Ebay() throws InterruptedException
	{ 
		
		File classpathRoot = new File(System.getProperty("user.dir"));
		  File app = new File(classpathRoot, "\\src\\app\\eBay.apk");
		  
		  
		  DesiredCapabilities caps = new DesiredCapabilities();	  
			caps.setCapability("deviceName","Redmi");
			//caps.setCapability("udid", "c87390670803"); 
			//293296680604
			caps.setCapability("udid", "293296680604");
			caps.setCapability("platformName", "Android");
			caps.setCapability("app", app.getAbsolutePath());
			caps.setCapability("platformVersion", "7.0");
			caps.setCapability("appPackage", "com.ebay.mobile");
			caps.setCapability("autoGrantPermissions", true);
			caps.setCapability("MobileCapabilityType", "100");
			caps.setCapability("noReset", false);
			
		//	AndroidDriver driver = null;
			try {
				driver = new AndroidDriver(new URL

("http://127.0.0.1:4723/wd/hub"), caps);} catch (MalformedURLException e) {
				// TODO Auto-generated catch block
				e.printStackTrace();
			}
			
	
           
			driver.manage().timeouts().implicitlyWait(50, 

TimeUnit.SECONDS);}
			
		   


@AfterTest
public void AfterMethod() throws InterruptedException
{ 
	
	// driver.quit();
	
	
}
}
