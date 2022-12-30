# rotten-tomatoes-ratings-to-letterboxd
JavaScript that you can use with a saved html page of your Rotten Tomatoes ratings in order to help convert them into csv format for import into Letterboxd.

This is some JavaScript I wrote to help recover your Rotten Tomatoes ratings data in order to import into Letterboxd.

You need to save the web page with your ratings as a .html file. The code uses DOM access to store all the ratings elements by looking for the class they share and then looping through each movie and adding the data to a JavaScript object and then converting that to JSON and pasting it into a paragraph tag at the bottom of the page that you can copy to a csv converter.

# requirements

- Code editor
- Web browser
- CSV converter (eg: one of the many free websites out there)
- Rotten Tomatoes account
- Letterboxd account

# how-to

1. Go to your Rotten Tomatoes profile page, click on Ratings tab, keep scrolling down to the bottom of the page until all ratings are loaded
2. Save the page as a file called ratings.html
3. Open both the ratings.html file and the index.html file in a code editor
4. Copy all the html tags of the ratings elements from the ratings.html file to the index.html file.
5. Open the index.html file in a browser
6. Copy the JSON data that should appear in a paragraph tag at the bottom of the web page
7. Paste into a csv converter website/app and save as a .csv file
8. make sure headings in .csv file match Letterboxd spelling/capitalisation requirements
9. Go to your Letterboxd settings and import the file

# known-issues

- Some people have reported that they can no longer load all their ratings by scrolling down on their profile page to load more.
- Spelling of the .csv headings needs to be changed to match Letterboxd
- Doesn't import reviews (just the ratings - but you could edit the code to do that too - I didn't have any reviews so didn't need to do it)
- Rotten tomatoes don't show up as a specific date (eg: "10 years ago"). So they are given a date of the end of that month or year so they are somewhat accurate. You may need to edit the code to add more cases to the switch statement than the date-range I used. Also, I didn't have any that said "weeks ago" or "days ago" but they can show up like that if recent ones so just add more cases to the switch statement if you need. I also used a default case to catch anything that didn't match my cases and date it as 1st December 2022 (you may wanna edit that to something that suits you more). Lastly, my dates given are based on estimates from the date of writing the code (so if you use this in the future, you will likely need to change the dates).
- Don't edit the csv in excel (it can change the data format to something that Letterboxd won't recognise (use Notepad or something)
