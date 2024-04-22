Quotes Management Application
Overview

This project is designed to create an application that allows users to store and browse quotes as per their preference. The main functionality includes adding new quotes along with their authors and displaying all saved entries. Additionally, as an extra feature, the client expects to see a "Quote of the Day" displayed on the form used for entering new quotes.
Features

    New Quote Submission Form & Saved Quotes List:
        A form for submitting new quotes and a list of saved quotes are provided on a single HTML page.
        A "GET" request to the path /quotes returns an HTML page containing the new quote submission form, the quote of the day, and all saved quotes.

    Saving Quotes:
        By clicking “Save Quote”, the entered data is sent to the server using the "POST" method of the HTTP protocol to the path /save-quote.
        The server stores the submitted data and redirects the client to /quotes to view the saved quote.

Technical Requirements

    System Architecture: The system is divided into two web services (main and auxiliary) that communicate over the HTTP protocol.
    Environment: Both applications run on localhost but listen on different ports.
    Main Service: Handles quote input, storage, and display to the client.
    Auxiliary Service:
        Has only one functionality, which is to return the "Quote of the Day."
        It should randomly select a quote from the existing set and return it in JSON format.
        This service is considered an internal service that does not communicate directly with the client but only with the main service. The main service requests the "Quote of the Day" from it to form the response to the client.
    Communication Protocol: Communication between services must be enabled using Java Socket without the use of pre-existing libraries (HTTP clients). Only libraries for parsing JSON are allowed.
