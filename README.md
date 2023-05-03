# Dangerous chemicals in presumptuve field tests

I went looking at the safety data sheets on a drug test manufacturer's website and noticed they all contain weirdly high concentrations of acids and other nasty chemicals. It turns out there are several groups trying to manufacture new kinds field tests and they specifically cite the harsh and carcinogenic chemicals in the ones currently in use.

I focused on the test manufacturer Sirchie because it's the provider for the Massachusetts prison system, which I've reported on before.

The assingment this time was to stretch ourselves and do something we hadn't done technically. For me, this took the form of using javascript, a language I have only used in code snippets and templates, to create scrollytelling and to construct elements on the page.

## Findings

All the field tests manufactured by Sirchie contain dangerous chemicals by the standards of the Globally Haronized System of Classification and Labelling of Chemicals (GHS). It's a standard created by the United Nations so chemicals are labeleld consistently in different countries' safety documentation.

Most of the tests contain chemicals in high enough concentrtions to cause severe skin burns and acute toxicity if inhaled. They are repeatedly used without safety equipment in uncontrolled settings like traffic stops and prison mailrooms.

## Data collection

Sirchie's safety data sheets are [here](https://www.sirchie.com/safety-data-sheets).

The GHS classification glossary is [here](http://www.ilpi.com/msds/ref/hstatements.html).

## Process and new skills

The scrollytelling work ended up taking a back seat to creating a grid that displayed all the images I wanted to be interactive. I used a relatively simply for loop to create a grid and populate each cell with an image.

After doing some analysis and deciding what I wanted to highlight, I needed there to be some information about the image that I could access with js in order to categorize it. Rather unelegantly, I put group names in the file names which could then be checked to add the appropriate class when loading the page.

But the way I wanted to draw attention to different tests, by turning down the opacity on ancillary ones, meant that I had to class images based on which groups they were *not* in and create an "anti-highlight" class that would be applied to all the tests outside of a certain group on each step. Messy. 

## Further work

This works, but it could be cleaner. Adding a csv to the docs folder that contains information about the test in each image would help. That way, the various relevant properties could be checked without long and irregular file names. A more direct highlighting system would also be nice. I'm not 100% sure how to do this while keeping the reduced opacity method, but maybe a grey overlay would be easier. I'm sure this will be straightforward as I become more familiar with the language.
