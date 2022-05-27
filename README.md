Step 1:
=======
Create a java package project name under src/test/java

Step 2:
=======
Create feature file with following code
  
Feature:   NSW Government media releases from selected ministers.

Scenario: Search media releases
    Given Navigate to [nsw.gov.au](https://www.nsw.gov.au/media-releases) 
    When I see an accordion named as “Filter by Minister” and inside the accordion, I see list of “Minister’s Name” with check boxes when accordion is expanded.
    And I select “The Premier” checkbox 
    And I can click “Search” button and media release item cards should be filtered based on Minister selected. 
    Then I want assert that filter is correctly applied on the item cards after “Search” button is clicked.
    
 Scenario: See reset button
    Given Navigate to [nsw.gov.au](https://www.nsw.gov.au/media-releases) 
    When I see an accordion named as “Filter by Minister” and inside the accordion, I see list of “Minister’s Name” with check boxes when accordion is expanded.
    And I select “The Premier” checkbox 
    And I can click “Search” button and media release item cards should be filtered based on Minister selected. 
    Then After “Search” button is clicked, I should see "Reset" button
