# Horoscoper

<!-- badges: start -->
<!-- badges: end -->

The goal of **horoscoper** is to provide detailed information about zodiac signs and horoscopes.  
This package uses web scraping to gather horoscope information from [horoscope.com](https://www.horoscope.com/us/index.aspx).

## Project Description

This project was developed as a collaborative effort between myself and two teammates. We aimed to create a package that simplifies the process of obtaining and interpreting daily horoscopes and zodiac information. My role involved writing the core functions, conducting web scraping for data collection, and ensuring package functionality.

### Key Features:

1. **Zodiac Sign Calculation**: Determine your zodiac sign based on your birthday.
2. **Zodiac Traits**: Learn about your sign's personality traits, lucky symbols, and compatibility.
3. **Daily Horoscope**: Get your daily horoscope based on your zodiac sign.
4. **Zodiac Compatibility**: Check the compatibility of any two zodiac signs.

Our teamwork focused on implementing these features efficiently and ensuring that the user can access accurate zodiac and horoscope information quickly.

## Installation

You can install the development version from [GitHub](https://github.com/) with:

```r
# install.packages("devtools")
devtools::install_github("aibarra21/horoscoper")
#> Using GitHub PAT from the git credential store.
#> Skipping install of 'horoscoper' from a github remote, the SHA1 (d287ed5c) has not changed since last install.
#>   Use `force = TRUE` to force installation

``` r
library(horoscoper)
```

## Zodiac Sign

You can use the function get_zodiac_sign() to determine what zodiac sign
you are by entering your birthday. Enter the month, day, then year in
any format.

``` r
get_zodiac_sign("april 24 2002")
#> [1] "Your zodiac sign is Taurus"
```

You can use the function get_sign_traits() to determine traits and
characteristics of your sign.

``` r
get_sign_traits("taurus")
#> Sign: Taurus
#> Symbol: Bull
#> Lucky Gem: Emerald
#> Flower: Rose, Poppy, & Foxglove
#> You are described as Dependable, Musical, Practical
#> You are most compatible with Cancer.
#> Motto: "Nothing worth having comes easy."
```

## Daily Horoscope

You can use the function getdailyhoroscope() to get your daily horoscope
for your zodiac. This function updates daily.

``` r
getdailyhoroscope("taurus")
#> Sign: Taurus
#> Daily Horoscope: May 29, 2024 - Your wacky personality will be appreciated today, Taurus, but don't take it too far. Leave room for seriousness to enter the picture. There's a dreamy, cloudy sensation to the day that might make it difficult for you to concentrate on any one thing. If you pretend to know the answer when you don't, you'll only confuse the people who rely on your knowledge or authority. Respect that everyone wants answers these days.
```

## Compatability

You can use the function compatibility() to determine how compatible any
two zodiac signs are.

``` r
compatibility("taurus","aries")
#> Romantic Compatibility between Taurus and Aries:
#> Compatibility Score: 4/10
#> Description: The Bull and the Ram are a hot-and-heavy couple from the start as each sign is sensual and passionate, which creates fireworks in bed.  However, there isn’t much going for the pairing.  The fiery temper of Aries clashes with the stubborn patience of Taurus, making fights a standoff.  Aries seeks change while Taurus craves routine.  Being one sign apart, they couldn’t be more different in terms of temperament and life views. Despite their glaring differences, the start of an Aries/Taurus paring is a beautiful thing: gushing compliments, gifts, vibrant conversation, and utter devotion.  As ambitious people, Taurus can help keep Aries steady and grounded while Aries can push the Bull to dream bigger.  Aries boldly seeks adventure and Taurus gives them a solid plan on how to get there—and a beautiful home to come back to.
```
