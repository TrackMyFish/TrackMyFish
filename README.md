<a href="https://www.buymeacoffee.com/simondrake" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" alt="Buy Me A Coffee" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a>
[![Gitter](https://badges.gitter.im/TrackMyFish/community.svg)](https://gitter.im/TrackMyFish/community?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)

# Introduction

TrackMyFish was designed to be a simple application to track fish for a home aquarium.

## What is the status of TrackMyFish?

The project is currently in an alpha stage. While we'll try our best not to introduce any breaking changes, it cannot be guaranteed until we reach v1.0.

## What can TrackMyFish do?

* Track your fish and see them in a nicely presented table
* Track your tank statistics (e.g. ammonia, nitrite, nitrate)
  * See your inputted tank statistics in graphical format, automatically

## Got any screenshots?

Sure...

![Fish Tracker](/assets/images/screenshots/trackmyfish1.png)
![Tank Statistic Tracker](/assets/images/screenshots/trackmyfish2.png)

# Running TrackMyFish

The easiest way of running TrackMyFish is using Docker. An example `docker-compose.yaml` file has been provided for this purpose.

**Note:** Because the migration image depends on the database being fully initialised, which doesn't happen straight away, the first call to `docker-compose` will fail. Just wait a couple of minutes and run it again, and it should succeed. This issue is being tracked in [#1](https://github.com/TrackMyFish/TrackMyFish/issues/1)

## Updating

```
docker-compose pull && docker-compose up -d && docker image prune -f
```

## Non-docker method

* Postgres should be running locally, and the [TrackMyFish migration package](https://github.com/TrackMyFish/db/blob/main/main.go) should be run to create the neccessary database configuration.
* Run the backend, by running `make run` from the [backend](https://github.com/TrackMyFish/backend) project
* Run the frontend, by running `npm start` from the [frontend](https://github.com/TrackMyFish/frontend) project

# Feedback

If you have any feedback, or want to see a new feature, please create an issue in this repository.
