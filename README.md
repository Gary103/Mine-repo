# Mine-repo
Test
public void CreateAgentOneFromRohansAccount()

	{
		System.setProperty("webdriver.chrome.driver", "C://Works//chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.get("http://stage-showpro.herokuapp.com/profile/admin_tools");
		driver.findElement(By.cssSelector("input[id='inputEmail']")).sendKeys("rohan.patil@anyonehome.com");
		driver.findElement(By.cssSelector("input[type ='password']")).sendKeys("@123");
		System.out.println(driver.findElement(By.xpath("//input[@name='remember']")).isSelected());// false
		driver.findElement(By.xpath("//input[@name='remember']")).click();
		System.out.println(driver.findElement(By.xpath("//input[@name='remember']")).isSelected());// true
		driver.findElement(By.xpath("//*[@id='content']/div/div/div/section/form/button")).click();
		driver.navigate().to(("http://stage-showpro.herokuapp.com/profile/admin_tools"));
		WebDriverWait wait = new WebDriverWait(driver, 20);
		wait.until(ExpectedConditions.visibilityOfElementLocated(By.xpath("//div [@id ='admin_tools_div']/section/section/section/header/ul/li[2]/a"))).click();
		driver.findElement(By.xpath("//div [@id ='admin_tools_div']/section/section/section/header/ul/li[2]/a")).click();
		driver.findElement(By.xpath("//div [@id = \"manage_users\"]/section/div/div/section/section/div/div/a")).click();
		driver.manage().window().maximize();
		WebDriverWait wait2 = new WebDriverWait(driver, 20);
		wait2.until(ExpectedConditions.visibilityOfElementLocated(By.id("addUserFirstName")));
		driver.findElement(By.id("addUserFirstName")).sendKeys("AutoAgentOne");
		driver.findElement(By.xpath("//input[@id='addUserLastName']")).sendKeys("AgentOne");
		driver.findElement(By.xpath("//input[@id='addUserEmail']")).sendKeys("11.ganesh@gmail.com");
		driver.findElement(By.xpath("//input[@id='addUserPassword']")).sendKeys("@123");
		driver.findElement(By.xpath("//button[@id='saveAddUserButton']")).click();
		
