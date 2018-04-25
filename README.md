# Table sorting with vanilla JS - made for a job interview

## Displaying Tabular Data with sorting
The decision making at Adgo is 100% based on data. One requirement is to be able to display
this data to users. The best and most classic way to do this, is by using tables. As a frontend
engineer, you might be asked to write a frontend component that takes in data and renders it to
a table that is sortable on all columns.

### Example

Given the following data:

"6069999532109": {
"status": 0,
"results": 1,
"impressions": 9,
"cpr": 0,
"reach": 0,
"spend": 0.27,
"end_date": 0,
"social_clicks": 0,
"action#video_view": 0,
"action#video_play": 0
}

We should be able to render a table with:
ID Status Result Impressions CPR Reach Spend End Date Social

## Your task
Create a frontend component that renders a table based on data that is coming back from our
APIs. You can find an example format here:
https://gist.github.com/briandeheus/ba212ad1659e4eecc2308e64cb3bec75
The amount of attributes returned to you might vary, but you can assume that each object contains the same attributes. For example if object ID 1001 has 2 attributes called ‘status’ and
‘result’, you can assume that all other objects have these 2 columns as well.

## Formatting

### Currencies
Columns that deal with currencies need to be formatted as a currency, this means you have to
prepend the dollar symbol to data. These columns are:
● Spend
● CPR

### Decimals
We should show up to 2 digits after the comma for all data points, if the value of a datapoint is a
float or a currency.

## Additional Columns
Besides the columns we deliver to you, you also need to display an additional column called
“ctr” if any of the following conditions is true:
There is an impressions and a social_clicks attribute present
There is an impressions and a clicks attribute presents
The click through rate (ctr) is a percentage, and this percentage can be calculated using the
following formula:
(100 / impressions) * clicks

## Sorting
It’s important that we can sort every column

## Styling
You are free to style the table as you see fit. The highest priority will be placed on functionality,
but being able to make the table look good is definitely a plus.
Technologies to be used
You can only use the most basic tools to complete this task. This means vanilla Javascript
(either ES5 or ES6), CSS and HTML. You can not use any frameworks.

## Deliver Format
You should deliver to us a single HTML file that contains the styles and javascript. Your page
should include a <textarea> element that can be used for data input, and a button to render the
actual table based on the data inside of the <textarea> element.
