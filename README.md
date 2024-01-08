# hepsiburada-data-scraping
you can  do web scraping for hepsiburada

firstly clone this repo after than

from hepsiburada_link_scraping import hepsiburada_data_extraction

from data_scraping import HepsiburadaDataExtractor

from data_scraping import toCsv

# step 1:

# data link scraping
base_url = "https://www.hepsiburada.com"
target_url = "https://www.hepsiburada.com/fritozler-c-22017"
target_class = 'VVfQFa_rVJ7k5k6NHFV3'
limit_page = 5


nesne = hepsiburada_data_extraction(base_url,target_url,target_class,limit_page)
nesne.run()

you can find target_class that way

![Ekran görüntüsü 2024-01-08 213731](https://github.com/thirtyfive-35/hepsiburada-data-scraping/assets/99458931/f8626cf1-99e5-478b-8a56-f8ee867bf836)

step 2:

# data scraping
base_url = "https://www.hepsiburada.com" 
target_class = "data-list tech-spec"  #you change that 
price_data_attribute = "markupText:'currentPriceBeforePoint'" #you change that 
product_name_selector = 'product-name best-price-trick' #you change that 

# Dosyadan linkleri oku
with open("dosya.txt", "r", encoding="utf-8") as dosya:
    links = dosya.read().splitlines()

extractor = HepsiburadaDataExtractor(base_url, target_class, price_data_attribute, product_name_selector)
extractor.run(links)

# txt to csv
toCsv()

To find target_class : 

![Ekran görüntüsü 2024-01-08 213905](https://github.com/thirtyfive-35/hepsiburada-data-scraping/assets/99458931/6945df36-8f63-4d36-8c4a-af23d21a5f01)


To find other options : 

![Ekran görüntüsü 2024-01-08 213959](https://github.com/thirtyfive-35/hepsiburada-data-scraping/assets/99458931/fd07cb88-7c3b-4ea0-bf50-b33e15fa60b6)

