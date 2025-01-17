# Selenium-WebDriver
My learnings on Selenium's Webdriver for Basic Scraping &amp; automations

#### References
https://youtube.com/playlist?list=PL6tu16kXT9PqixJLqvRWDIIOtGJTzOpQG&si=kZ1skI0oxriVJXX8

https://youtube.com/playlist?list=PLnNg6KqJ3HGh8K2KhCCxraHh09L3LPL4E&si=oQRjJLLm-cfoSX0O

https://www.selenium.dev/documentation/webdriver/getting_started/

---

# Components of Selenium Suite

Selenium IDE

Selenium Grid

Selenium Webdriver

Selenuim RC (merged to Selenium 3)

# Selenium WebDriver

Component of Selenium suite to interact with web elements

it’s a Java Interface, implemented by browser class

It’s an API, ie mediator btw browser & client libraries

# Architecture

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/ea4cd4e4-283b-433d-a65e-80e280a71973/8a641e7e-3e0a-4004-8057-3209c5114c01/659a8289-f5da-4db1-91f5-15e30c161086.png)

# Installation

for maven paste selenium webdriver dependencies in pom.xml

---

# **Waiting Strategies**

https://www.selenium.dev/documentation/webdriver/waits/

---

# Locators

## Basic locators

1. By ID
2. By name
3. By class name
4. By tag name
5. By link text
6. By partial link text

## Custom locators by `CSS Selectors`

| HTML Tag, id, class, attribute combination | Syntax | Example |
| --- | --- | --- |
| Tag & id | **`tag#id`**  | **`driver.findElement(By.*cssSelector*("input#user-name"));`** |
| tag & class | **`tag.class`** | **`driver.findElement(By.*cssSelector*("input.Username"));`** |
| tag & attribute | **`tag[attribute=value]`** | **`driver.findElement(By.*cssSelector*("input[name=user-name]"));`** |
| tag, class & attribute | **`tag.class[attribute=value]`** | **`driver.findElement(By.*cssSelector*("button.btn[name=add-to-cart-backpack]"));`** |
| Sub-string method | **- starts with `=^`  
- end with `=$` 
- contains `=*` 
- `tag[attribute^=substring]`** | Find something unique and target with substring

**`driver.findElement(By.*cssSelector*("button[name$=light]"));`** |

## Custom locators by `XP**ath`**

XPath → XML Path

It’s a query language to locate nodes in XML document

It gives the absolute/relative address of WebElement in dom tree

**`Absolute XPath` `Relative XPath` `Single Attribute` `Multiple Attribute` `AND` `OR` `contains()` `starts_with()` `text()` `position()` `last()`** 

Relative XPath is most used

### Absolute XPath

It begins from **`root`** of DOM, & traces till the node element

starts with **`/`** symbol

e.g. **`/html[1]/body[1]/div[1]/div[1]/div[2]/div[1]/div[1]/div[1]/form[1]/input[1]`** 

### Relative XPath

relative xpath begins from the element to be located and not from the root

unlike Absolute XPath it starts with **`//`** symbol

syntax: **`//tagname[@attribute name=’attribute-value’]`**

e.g. **`//input[@id='login-button']`** 

**Relative XPath using single attribute**

**`//<HTML tag>[@attribute_name='attribute_value']`  or `//*[@attribute_name='attribute_value']`** 

**XPath using multiple attributes**

**`//<HTML tag>[@attribute_name1='attribute_value1'][@attribute_name2='attribute_value2']` or**

**`//*[@attribute_name1='attribute_value1'][@attribute_name2='attribute_value2']`** 

<aside>
💡

**`*`**  is to match any tag

</aside>

- Example
    
    

---
