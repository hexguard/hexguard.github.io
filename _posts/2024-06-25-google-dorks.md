---
title : Beginner's guide to Google Dorks
date : 2024-06-25 1:00:00 +07:00
tags : [ "Google", "Dorks", "Search", "Penetration Testing"]
categories : [ "Penetration Testing" ]
---

# Beginner Guide to Google Dorks

![Google Dorks](assets/google dorks.png){: width="600" height="400" }

A "Google Dork" is an advanced Google search technique. "Google Dorking" is the activity of performing advanced searches on Google. These terms, also termed advanced Google operators, provide the exact information. It reduces the search time by instantly providing the information as we don't have to move from one page to another. These operators work as queries. 

## Information Dorks

These dorks appear to work best if used as standalone commands without additional query items.

* **cache:** Get Google's last saved version of a particular website. A website snapshot like this is called "cache".
    * Eg: `cache:blog.google`
* **link:** Find pages linking to the given domain.
    * Eg: `link:Harvard.edu`
* **related:** Return websites related to the given website.
    * Eg: `related:bbc.co.uk`
* **map:** Get a map of the given location.
    * Eg: `map: 'new York'`
* **weather:** Get the weather of the given location.
    * Eg: `weather:london`
* **location:** Find information about a location. Results may be inconsistent.
    * Eg: `location:NY`
* **info:** Return pages that convey information about the given website.
    * Eg: `info:google.com`

## Google Dorks Operators

### Search Operators

These refine the search and constrain the results to follow logic rules. Most of the following are logical operators.

* **OR, \|** Return sites containing either query item joined by OR or the pipe character \|. This is an inclusive OR.
    * Eg: `Amazon OR Google`, `Amazon | Google`
* **( )** Group multiple Google dork operators as a logical statement.
    * Eg: `(black OR white) hat hacker`
* **-** Hyphen; exclude search results containing the word or phrase after the hyphen.
    * Eg: `Amazon -reviews`, `"sql injection" -"penetration testing"`
* **#..#** Search a numerical range specified by the two endpoints. 
    * Eg: `2006..2008` finds all pages that include 2006, 2007, or 2008 in them.

### Math Operators

* **+** Addition
    * Eg: `5 + 3 = 8`
* **-** Subtraction
    * Eg: `10 - 4 = 6`
* **\*** Multiplication
    * Eg: `6 * 7 = 42`
* **/** Division
    * Eg: `20 / 4 = 5`
* **% of** Percentage
    * Eg: `50% of 200 = 100`
* **X^Y, X**Y** Raise X to the power of Y. Both operators ^ and ** perform the same operation.
    * Eg: `3 ^ 2`, `3 ** 2 = 9`
* **in, to** Convert a quantity from a given unit to another. Translate words into another language.
    * Eg: `10 cm in inches`, `100 dollars to euros`
* **Sqrt** Square root
    * Eg: `sqrt(25) = 5`
* **N choose R** Find how many combinations are possible from N items taken R at a time, where N and R are integers. (Combinatorics)
    * Eg: `6 choose 4 = 15`

## Text Dorks

These are helpful if you want to look for web pages containing certain text strings or follow particular patterns.

* **intitle:** This query will return the pages that include the "target_word".
    * Eg: `intitle:hacking`
* **inurl:** This query will return the pages that include the target_word in its URL.
    * Eg: `inurl:login.php`
* **allinurl:** Find the links containing all words in the colon(:). Also equivalent to applying "inurl:" to discrete search strings.
    * Eg: `allinurl:healthy foods`

## Scope-Restricting Dorks

These help specify your target range of websites or data types.

* **site:** Restrict search to particular websites, top-level domains, or subdomains.
    * Eg: `site:maps.google.com`
* **filetype:, ext:** The filetype: ext: operators allow users to search for specific types of files on the web.  This is particularly useful for documents, PDFs, or other specific file formats. 
    * Eg: `cybersecurity filetype:pdf`
* **@** Restrict search to a particular social platform. It supports popular platforms like Facebook, Twitter, YouTube, and Reddit.
    * Eg: `cybersecurity @reddit`
* **define:** Return Definitions of a word or phrase.
    * Eg: `define:cybersecurity`
* **source:** Find reports from a Google News source.
    * Eg: `source:cnn`

## Advantages

* These operators provide the exact results that we are looking for.
* There is no wastage of time as there is no redirecting from one page to another.