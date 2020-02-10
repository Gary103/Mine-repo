# Mine-repo
Test

public void CreateLeadOneFromRohansAccount() throws InterruptedException {
		System.setProperty("webdriver.chrome.driver", "C://Works//chromedriver.exe");

		WebDriver driver = new ChromeDriver();
		System.out.println("URL Test for Anyone Home Stage environment");
		driver.get("http://stage-showpro.herokuapp.com/signin");
		String title = driver.getTitle();
		boolean expected = title.contains("Anyone Home CRM 3.1.20");
		assertTrue(expected, "Title is verified");
		driver.findElement(By.cssSelector("input[id='inputEmail']")).sendKeys("rohan.patil@anyonehome.com");
		driver.findElement(By.cssSelector("input[type ='password']")).sendKeys("@123");
		System.out.println(driver.findElement(By.xpath("//input[@name='remember']")).isSelected());// false
		driver.findElement(By.xpath("//input[@name='remember']")).click();
		System.out.println(driver.findElement(By.xpath("//input[@name='remember']")).isSelected());// true
		driver.findElement(By.xpath("//*[@id='content']/div/div/div/section/form/button")).click();
		driver.findElement(By.xpath("//b[@class='caret hidden-xs-only']")).click();
		driver.manage().window().maximize();
		System.out.println(driver.getTitle());
		driver.findElement(By.linkText("Create")).click();
		driver.findElement(By.xpath("//input[@id='event_first_name']")).sendKeys("AutoLeadTest");
		driver.findElement(By.xpath("//input[@id='event_last_name']")).sendKeys("One");
		driver.findElement(By.xpath("//input[@id='event_mobile']")).sendKeys("9495551806");
		driver.findElement(By.xpath("//div[@id ='property_selection']/div[1]/div/a")).click();
		driver.findElement(By.xpath("//div[@id='select2-drop']/div/input")).sendKeys("sitka");
		Thread.sleep(3000);
		driver.findElement(By.xpath("//*[@id='select2-results-2']/li[2]")).click();
		driver.findElement(By.xpath("//div[@id='source_type_id']")).click();
		Thread.sleep(3000);
		driver.findElement(By.xpath("//*[@id=\"select2-drop\"]/div/input")).sendKeys("mitch");
		Thread.sleep(3000);
		driver.findElement(By.xpath("//*[@id=\"select2-drop\"]/div/input")).sendKeys(Keys.DOWN);
		driver.findElement(By.xpath("//*[@id=\"select2-drop\"]/div/input")).sendKeys(Keys.ENTER);
		driver.findElement(By.xpath("//button[@id='save_btn']")).click();
	
