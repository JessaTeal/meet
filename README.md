Welcome to my MeetUp app!

This app will be a progressive web application utilizing React and the test-driven development technique.

This app will allow users to view events happening around them

Testing Parameters:

FEATURE 1: SHOW/HIDE AN EVENT'S DETAILS

Scenario 1: When user hasn't searched for a city, show upcoming events from all cities
    As a user, I should be able to leave the city parameter empty so that I can view all events in all cities
    Given user hasn’t searched for any city
    When the user opens the app
    Then the user should see a list of all upcoming events

Scenario 2: User should see a list of suggestions when they search for a city
    As a user, I should be able to see suggested cities when I search so that I can select the correct city
    Given the main page is open
    When user starts typing in the city textbox
    Then the user should see a list of cities (suggestions) that match what they’ve typed

Scenario 3: User can select a city from the suggested list
    As a user, I should be able to select a city so that I can view the events happening in that city
    Given the user was typing “Berlin” in the city textbox
    And the list of suggested cities is showing
    When the user selects a city (e.g., “Berlin, Germany”) from the list
        Then their city should be changed to that city (i.e., “Berlin, Germany”)
        And the user should receive a list of upcoming events in that city


FEATURE 2: SHOW/HIDE AN EVENT'S DETAILS

Scenario 1: An event element is collapsed by default
    As a user, I should be able to load the webpage so that event details are not shown until selected
    Given the user has not selected an event
    When the user is viewing the webpage
    Then the details of an even is not shown until selected

Scenario 2: User can expand an event to see its details
    As a user, I should be able to click on “Show details” of an event so that I can view the event details
    Given the page has loaded the list of events
    When the user clicks on “Show details” to view the event
    Then the event will be expanded and show the details of the event

Scenario 3: User can collapse an event to hide its details
    As a user, I should be able to collapse an events details so that the details are not shown on the page
    Given the user has an event details open
    When the user selects “hide details”
    Then the event details will be removed from the view


FEATURE 3: SPECIFY NUMBER OF EVENTS

Scenario 1: When user hasn’t specified a number, 32 is the default number
    As a user, I should be able to put no parameters on event view so that the page will default to 32 events
    Given the user has not specified the number of events   
    When the user searches for a number of events
    Then 32 events will default to the view

Scenario 2: User can change the number of events they want to see
    As a user, I should be able to set view filters so that I can see as many events as I want to
    Given the user wants to see a specific number of events
    When the user specifies a number
    Then that many views will show on the screen


FEATURE 4: USE THE APP WHEN OFFLINE

Scenario 1: Show cached data when there’s no internet connection
    As a user, I should be able to view information offline so that when no internet is available I can view my stored information
    Given the user is offline
    When the user views the app
    Then they are able to see their saved data

Scenario 2: Show error when user changes the settings (city, time range)
    As a user, I should be able to alerted when I change settings so that I am seeing the events in the city I prefer
    Given the user has been viewing events in one city
    When the city information is changed
    Then the user is alerted to the change


FEATURE 5: DATA VISUALIZATION
Scenario 1: Show a chart with the number of upcoming events in each city
    As a user, I should be able to see a chart with how many events in each city so that I can see which city I hosting more events
    Given the user has selected the graph view
    When the user selects event details
    Then they can see which city is hosting more of each kind of event 