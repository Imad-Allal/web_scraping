# Data Scraper: Woolworths

## About The Project
The [Woolworths](https://www.woolworths.com.au/) Data Scraper is a custom-built project designed to extract detailed information about laundry articles and their prices from the Woolworths website. With a focus on laundry products, this scraper gathers valuable data that can benefit businesses and individuals in the [laundry](https://www.woolworths.com.au/shop/browse/cleaning/laundry) industry, as well as consumers seeking information on pricing and product options.

## Built With
[Selenium](https://www.selenium.dev/documentation/)

## Getting Started
*To get started, follow these steps:

**1) Install the [Selenium](https://www.selenium.dev/documentation/) package on your device**
```bash
!pip install selenium
```
**2) Clone the repo**
```bash
git clone https://github.com/Imad-Allal/web_scraping
```
**3) Run the .ipynb file**
```bash
python3 dataScraping.ipynb
```

### OR instead, you can simply use [Docker](https://www.docker.com/)
**1) Build the Dockerfile**
```bash
docker build -t selenium-notebook .
```
**2) Run the DockerFile**
```bash
docker run -p 1313:1313	 -v /path/to/notebooks:/app/notebooks selenium-notebook
```
**Note:** Don't forget to replace /path/to/notebooks by the path to the directory on your host machine where you want to store your notebooks. 

## Understanding The Code
![carbon](https://github.com/Imad-Allal/web_scraping/assets/80546947/18ca4b21-07d6-468f-9e71-6a0fbd55c8bb)
``prices = driver.find_elements(By.CLASS_NAME, "product-information-container")``
This line finds all the web elements on the page that have the class name "product-information-container" and stores them in the prices variable. These elements likely represent the prices of different products.

``products = driver.find_elements(By.CLASS_NAME, "product-title-container")``
This line finds all the web elements on the page that have the class name "product-title-container" and stores them in the products variable. These elements likely represent the titles or names of different products.

``data = []``
This line initializes an empty list called data to store the extracted information.

The code then enters a loop using ``enumerate(products)`` to iterate over each product element and its corresponding index.

``data.append({prdct.text: prices[i].text})``
Inside the loop, this line creates a dictionary where the key is the text of the current product element (prdct.text) and the value is the text of the corresponding price element (prices[i].text). The dictionary is then appended to the data list.

``json_data = json.dumps(data)``
Finally, this line converts the data list into a JSON string representation using the json.dumps() function. The resulting JSON string, json_data, can be used to store or transmit the extracted data in a structured format.

## Contact
[LinkedIn](https://www.linkedin.com/in/imad-allal-106653204/)

[pro.imadallal@outlook.com](mailto:pro.imadallal.com)

## Project Link
https://github.com/Imad-Allal/web_scraping


