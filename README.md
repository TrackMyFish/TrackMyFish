# Introduction

TrackMyFish was designed to be a very simple application to track fish for a home aquarium.

## What is the status of TrackMyFish?

The project is currently in an alpha stage. While we'll try our best not to introduce any breaking changes, it cannot be guaranteed until we reach v1.0.

## Why would I use this instead of a Spreadsheet?

The main advantage is the TrackMyFish integration with FishBase to autopopulate information (e.g. Ecosystem name, type and location). Over time more improvements will be made.

## Got any screenshots?

Sure...

![screenshot one](/assets/images/screenshots/trackmyfish1.png)

# Running Locally

Currently, the only way to run TrackMyFish is to run each component (frontend and backend) individually. In the near future, the frontend will be compiled and served from the backend, and TrackMyFish will be dockerized.

## Pre-requisites

* Postgres should be running locally, and the [TrackMyFish migration package](https://github.com/TrackMyFish/db/blob/main/main.go) should be run to create the neccessary database configuration.
  * Note: Currently, the database credentials are hardcoded in `main.go`, this will be served from a config file in the future.
* Run the backend, by running `make run` from the [backend](https://github.com/TrackMyFish/backend) project
* Run the frontend, by running `npm start` from the [frontend](https://github.com/TrackMyFish/frontend) project

# Tips and Tricks

## How do I find the Genus and Species of my fish?

Under `Useful Links`, in the Navbar, there is a link to Fishbase; where you can search for your fish by it's common name. For example:

* Search for "Guppy"
* Fishbase returns the Species as "Poecilia reticulata" where "Poecillia" is the Genus and "reticulata" is the Species.

In the future, we aim to add this functionality directly into TrackMyFish to avoid having to go to a separate website.

# Feedback

If you have any feedback, or want to see a new feature, please create an issue in this repository.