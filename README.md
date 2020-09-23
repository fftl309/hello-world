package ru.Rambler;

import org.junit.Test;
import org.openqa.selenium.By;
import org.openqa.selenium.chrome.ChromeDriver;

public class Pochta {

      @Test
    public void Pochta() throws InterruptedException {
          System.setProperty("webdriver.chtome.driver","/Webdrivers/chromedriver.exe");
          ChromeDriver driver = new ChromeDriver();
          driver.manage().window().maximize();
          driver.get("https://id.rambler.ru/login-20/login?back=https%3A%2F%2Fwww.rambler.ru&rname=head&type=self");
          Thread.sleep(2000);
          driver.findElement(By.id("login")).sendKeys("test27041998@rambler.ru");
          driver.findElement(By.id("password")).sendKeys("Tttttttttt1234567890");
          driver.findElement(By.xpath("//span[contains(text(), 'Войти')]")).click();
          Thread.sleep(2000);
          driver.get("https://mail.rambler.ru/folder/INBOX/?utm_source=head&utm_campaign=self_promo&utm_medium=widget&utm_content=mail&utm_term=inbox");
          driver.findElement(By.xpath("//span[contains(text(), 'Написать')]")).click();
          driver.findElement(By.id("receivers")).sendKeys("fftl309@yandex.ru");
          driver.findElement(By.id("subject")).sendKeys("Собеседование");
          driver.findElement(By.id("editor_ifr")).sendKeys("https://github.com/fftl309 , Гусаков Александр Сергеевич");
          driver.findElement(By.xpath("//span[contains(text(), 'Отправить')]")).click();
          Thread.sleep(3000);
          driver.quit();



      }
}
