# World Countries: Multilingual World Country Basic Info

A python package for retrieving basic data from all countries in the world in the most popular languages: English, Chinese, Spanish, Arabic, French, Russian, German.


## Install

```python
pip install world-countries
```

## Usage

### Multilingual API

The package provides country data in multiple languages. You can import the module in different languages to get country names and information in that specific language.

Translated attributes:
- country name
- country capital
- continent name
- region name

```python
# default (english)
import world_countries as wc

print(wc.countries()) 

```

```python
['Afghanistan', 'Albania', 'Algeria', 'Andorra', 'Vietnam', 'Yemen', 'Zambia', 'Zimbabwe'] 
```

```python
# russian
import world_countries.ru as wc

print(wc.countries()) 

```

```python
['Афганистан', 'Албания', 'Алжир', 'Андорра', 'Вьетнам', 'Йемен', 'Замбия', 'Зимбабве'] 
```

```python
# arabic
import world_countries.ar as wc

print(wc.countries()) 

```

```python
['أفغانستان', 'ألبانيا', 'الجزائر', 'أندورا', 'فيتنام', 'اليمن', 'زامبيا', 'زيمبابوي']
```

### Functions

- [countries()](#countries)
- [get_country_info()](#get_country_info)
- [phone_code()](#phone_code)
- [currencies()](#currencies)
- [capitals()](#capitals)  
- [continents()](#continents)   
- [countries_in_continents()](#countries_in_continents)
- [search_by_continent()](#search_by_continent)
- [regions()](#regions)
- [countries_in_region()](#countries_in_region) 
- [search_by_region()](#search_by_region)
- [languages()](#languages)
- [get_languages_by_country()](#get_languages_by_country)
- [search_by_language()](#search_by_language)


### .countries()
Returns the list of all available countries in the world

```python
import world_countries as wc

print(wc.countries()) 

```

```python
['Afghanistan', 'Aland Islands', 'Albania', 'Algeria', 'American Samoa', 'Andorra', 'Angola', 'Anguilla', 'Antarctica', 'Antigua And Barbuda', 'Argentina', 'Armenia', 'Aruba', 'Australia', 'Austria', 'Azerbaijan', 'Bahamas The',  'Vietnam', 'Virgin Islands (British)', 'Virgin Islands (US)', 'Wallis And Futuna Islands', 'Western Sahara', 'Yemen', 'Zambia', 'Zimbabwe'] 
```

### .get_country_info()
Returns complete information about a specific country by its name

```python
import world_countries as wc

print(wc.get_country_info('Serbia')) 

```

```python
{'id': 196, 'name': 'Serbia', 'iso3': 'SRB', 'iso2': 'RS', 'phone_code': '381', 'capital': 'Belgrade', 'currency': 'RSD', 'native': 'Србија', 'emoji': '🇷🇸', 'emojiU': 'U+1F1F7 U+1F1F8', 'continent': 'Europe', 'region': 'Southern Europe', 'languages': ['sr']}
```

### .phone_code()
Returns phone codes of each country in a dictionary

```python
import world_countries as wc

print(wc.phone_code()) 

```

```python
{'Afghanistan': '93', 'Aland Islands': '+358-18', 'Albania': '355', 'Algeria': '213', 'American Samoa': '+1-684', 'Andorra': '376', 'Angola': '244', 'Anguilla': '+1-264', 'Antarctica': '', 'Antigua And Barbuda': '+1-268', 'Argentina': '54', 'Armenia': '374', 'Aruba': '297', 'Australia': '61', 'Austria': '43', 'Azerbaijan': '994', 'Bahamas The': '+1-242', 'Bahrain': '973', 'Bangladesh': '880'}
```

### .currencies()
Returns currencies of each country in a dictionary

```python
import world_countries as wc

print(wc.currencies()) 

```

```python
{'Afghanistan': 'AFN', 'Aland Islands': 'EUR', 'Albania': 'ALL', 'Algeria': 'DZD', 'American Samoa': 'USD', 'Andorra': 'EUR', 'Angola': 'AOA', 'Anguilla': 'XCD', 'Antarctica': '', 'Antigua And Barbuda': 'XCD', 'Argentina': 'ARS', 'Belgium': 'EUR', 'Belize': 'BZD', 'Benin': 'XOF', 'Bermuda': 'BMD', 'Bhutan': 'BTN', 'Bolivia': 'BOB', 'Bosnia and Herzegovina': 'BAM', 'Botswana': 'BWP'}
```

### .capitals()
Returns capital cities of each country in a dictionary

```python
import world_countries as wc

print(wc.capitals()) 
```

```python
{'Afghanistan': 'Kabul', 'Aland Islands': 'Mariehamn', 'Albania': 'Tirana', 'Algeria': 'Algiers', 'American Samoa': 'Pago Pago', 'Andorra': 'Andorra la Vella', 'Angola': 'Luanda', 'Anguilla': 'The Valley', 'Antarctica': '', 'Antigua And Barbuda': "St. John's",  'Bahamas The': 'Nassau', 'Bahrain': 'Manama', 'Bangladesh': 'Dhaka', 'Barbados': 'Bridgetown', 'Belarus': 'Minsk', 'Belgium': 'Brussels', 'Belize': 'Belmopan'}
```

### .continents()
Returns continents of each country

```python
import world_countries as wc

print(wc.continents()) 
```

```python
[{'country': 'Afghanistan', 'continent': 'Asia'}, {'country': 'Albania', 'continent': 'Europe'}, {'country': 'Algeria', 'continent': 'Africa'}, {'country': 'American Samoa', 'continent': 'Oceania'}, {'country': 'Andorra', 'continent': 'Europe'}, {'country': 'Angola', 'continent': 'Africa'}, {'country': 'Anguilla', 'continent': 'North America'},{'country': 'Antarctica', 'continent': 'Antarctica'}]
```

### .countries_in_continents()
Returns a list of countries present in each continent

```python
import world_countries as wc

print(wc.countries_in_continents()) 
```

```python
{'Asia': ['Afghanistan', 'Armenia', 'Azerbaijan', 'Bahrain', 'Bangladesh', 'Bhutan', 'Brunei', 'Cambodia', 'China', 'Cyprus', 'East Timor', 'Georgia', 'Hong Kong', 'India', 'Indonesia', 'Iran', 'Iraq', 'Israel', 'Japan', 'Jordan', 'Kazakhstan', 'Kuwait', 'Kyrgyzstan', 'Laos', 'Lebanon',   'Tajikistan', 'Thailand', 'Turkey', 'Turkmenistan', 'United Arab Emirates', 'Uzbekistan', 'Vietnam', 'Yemen']}
```

### .search_by_continent()
Returns all countries in a specific continent

```python
import world_countries as wc

print(wc.search_by_continent('Asia')) 
```

```python
['Afghanistan', 'Armenia', 'Azerbaijan', 'Bahrain', 'Bangladesh', 'Bhutan', 'Brunei', 'Cambodia', 'China', 'Cyprus', 'East Timor', 'Georgia', 'Hong Kong', 'India', 'Indonesia', 'Iran', 'Iraq', 'Israel', 'Japan', 'Jordan', 'Kazakhstan', 'Kuwait', 'Kyrgyzstan', 'Laos', 'Lebanon',   'Tajikistan', 'Thailand', 'Turkey', 'Turkmenistan', 'United Arab Emirates', 'Uzbekistan', 'Vietnam', 'Yemen']
```

### .regions()
Returns countries with its region

```python
import world_countries as wc

print(wc.regions()) 
```

```python
[{'country': 'Afghanistan', 'location': 'Southern and Central Asia'}, {'country': 'Albania', 'location': 'Southern Europe'}, {'country': 'Algeria', 'location': 'Northern Africa'}, {'country': 'American Samoa', 'location': 'Polynesia'}, {'country': 'Andorra', 'location': 'Southern Europe'}, {'country': 'Aruba', 'location': 'Caribbean'}, {'country': 'Australia', 'location': 'Australia and New Zealand'}]  
```

### .countries_in_region()
Returns the list of countries in a region in a dictionary

```python
import world_countries as wc

print(wc.countries_in_region()) 
```

```python
{'Antarctica': ['Antarctica', 'Heard Island and McDonald Islands', 'South Georgia and the South Sandwich Islands'], 'Eastern Europe': ['Belarus', 'Hungary', 'Moldova', 'Poland', 'Romania', 'Ukraine'], 'Southern Europe': ['Albania', 'Andorra',   'Italy', 'North Macedonia', 'Yugoslavia'], 'Western Europe': ['Austria', 'Belgium', 'France', 'Germany', 'Liechtenstein',  'Switzerland'], 'North America': ['Bermuda',  'United States']}
```

### .search_by_region()
Returns all countries in a specific region

```python
import world_countries as wc

print(wc.search_by_region('Eastern Europe')) 
```

```python
['Belarus', 'Bulgaria', 'Czech Republic', 'Hungary', 'Moldova', 'Poland', 'Romania', 'Russia', 'Slovakia', 'Ukraine']
```

### .languages()
Returns the countries and their language codes

```python
import world_countries as wc

print(wc.languages()) 
```

```python
{'Afghanistan': ['ps', 'uz', 'tk'], 'Aland Islands': ['sv'], 'Albania': ['sq'], 'Algeria': ['ar'], 'American Samoa': ['en', 'sm'], 'Andorra': ['ca'], 'Angola': ['pt'], 'Anguilla': ['en'], 'Antarctica': [], 'Antigua And Barbuda': ['en'], 'Argentina': ['es', 'gn'], 'Armenia': ['hy', 'ru'], 'Aruba': ['nl', 'pa'], 'Australia': ['en']}
```

### .get_languages_by_country()
Returns language codes for a specific country

```python
import world_countries as wc

print(wc.get_languages_by_country('Nauru')) 
```

```python
['en', 'na']
```

### .search_by_language()
Returns all countries that speak a specific language code

```python
import world_countries as wc

print(wc.search_by_language('es')) 
```

```python
['Argentina', 'Belize', 'Bolivia', 'Chile', 'Colombia', 'Costa Rica', 'Cuba', 'Dominican Republic', 'Ecuador', 'El Salvador', 'Equatorial Guinea', 'Guam', 'Guatemala', 'Honduras', 'Mexico', 'Nicaragua', 'Panama', 'Paraguay', 'Peru', 'Puerto Rico', 'Spain', 'Uruguay', 'Venezuela', 'Western Sahara']
```


## Created & Maintained By

### [g2r4i6e8](https://github.com/g2r4i6e8)

Andrey Kolomatskiy

<a href="https://www.linkedin.com/in/akolomatskiy/" target="_blank"><img src="https://github.com/aritraroy/social-icons/blob/master/linkedin-icon.png?raw=true" width="60"></a>

## Credits

This is the fork of the repository originally created by [Manumanoj](https://github.com/manumanoj0010)
