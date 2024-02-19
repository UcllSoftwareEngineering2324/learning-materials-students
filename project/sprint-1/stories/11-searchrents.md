# Search Rents

As a user\
I want to search for certain rents\
So that I can see all my rents or all rents by a renter with a specific email address

## Mock-up

<a href="./mockups/searchrents.jpg">
    <img src="./mockups/searchrents.jpg" width=200>
</a>

## Acceptance Criteria
* **Given** the user chooses an email\
**And** there exist a renter of rents with this email address\
**When** the user searches\
**Then** the rents of the renter with this email address are given as a result

* **Given** the user chooses no values\
**When** the user searches\
**Then** an error message "You need to choose one or more values to get search results" is given
