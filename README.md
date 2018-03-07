# Project Overview

The tests are divided into four test suites, each with different purposes. They will run all run when the page initial loads. To do that please begin by opening index.html on a web browser such as Google Chrome or Safari. The descriptions for each test suite are as follows:

## RSS Feeds

These tests will make sure that the requirements of all feeds are met; which consists of an array containing objects that have a URL and name of that page.


## The Menu

The menu should be hidden by default and will only appear when toggled. To test if this works we run jQuery calls to first make sure it is hidden when the page loads. Then we toggle to make it appear and test that it is so. Finally we toggle the button to make it hidden again, and test for that. The most obvious way of detecting if the menu is hidden is by checking the body class to see if the attribute "menu-hidden" is stated there. If it is then then the menu is hidden.


## Initial Entries

This test makes sure that after an async load there's at least one entry listed. This test gets a little more complicated and requires the usage of a beforeEach function that runs before any tests are initiated. In beforeEach() we load the feed with the first page. After the load is complete with state it so with a done() command that allows the tests to begin. In this test we run a count on the number of entries that now exist by pulling it from the element tags labeled with an "entry" class. If the count is greater than 0 then the test passes.


## New Feed Selection

The final test checks that new values are inputed when the page changes. The best way to check that the values are different is by checking the header, which changes as pages change. We begin the test by loading feed for the first page and checking that the header is "Udacity Blog". Afterwards we load the second page and check if the header is "CSS Tricks". 

# Additional Notes
After completing the tests we reset the view to its default settings by loading the first page. Results of the test will be seen on the bottom. 