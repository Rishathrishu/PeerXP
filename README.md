# PeerXP
Regarding interview

import org.openqa.selenium.By;
import org.openqa.selenium.Keys;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;

public class PeerXPDemo {

	public static void main(String[] args) throws InterruptedException {
		
		System.setProperty("webdriver.chrome.driver", "D:\\Java\\Chrome\\chromedriver.exe");
		WebDriver d = new ChromeDriver();
		d.manage().deleteAllCookies();
		d.manage().window().maximize();
		d.get("http://www.yatra.com/");
		Thread.sleep(3000);
		d.findElement(By.xpath("//input[@id='BE_flight_origin_city']")).click();
		d.findElement(By.xpath("//input[@id='BE_flight_origin_city']")).sendKeys("bangalore");
		d.findElement(By.xpath("//input[@id='BE_flight_origin_city']")).sendKeys(Keys.ENTER);
		
		d.findElement(By.xpath("//input[@id='BE_flight_arrival_city']")).click();
		d.findElement(By.xpath("//input[@id='BE_flight_arrival_city']")).sendKeys("delhi");
		d.findElement(By.xpath("//input[@id='BE_flight_arrival_city']")).sendKeys(Keys.ENTER);
		

	}

}

