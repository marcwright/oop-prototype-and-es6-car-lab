# Prototype + ES6 Classes Body Shop

The idea of this lab is to get you comfortable with Object Oriented Programming (OOP) and introduce you to Test Driven Development (TDD) in JavaScript. By the end you should be comfortable working with objects and writing prototypes.

All of the tests have been written for you, so all you'll need to do is run them. No need to create any Car objects, because the tests will do that for you.

If any of the tests errors are unclear, take a look at what the test is running within `test/carTest.js`

<br>

## Getting Started

* Fork and clone this repository
* Run `npm install` to install dependencies
* `npm test` - run test suite

<br>

## Submission

Fork and clone this repo. Push to your repo and submit a pull request when you're done.

**You only need to add code to `src/Car.js`**  Run the tests and make sure they all pass. You should have **13** `...success` messages after running your code.  Your successful code should look like so:

![](https://i.imgur.com/w60WywC.png)

<br>

## Requirements

We need a prototype for a car. Can you help us with your sweet JavaScript skills?

### Phase I

Your `Car` should meet the following requirements:

* Must have the following constructor parameters:
  * `make`
  * `model`
  * `year`
  * `color`
  * `seats`
* By default, a new `Car` should have the following values **initialized** in the constructor:
  * `previousOwners`
    * should be initialized to an empty array, `[]`.
  * `owner`
    * should be initialized to 'manufacturer'.
  * `running`
    * should be initialized to `false`.
* We should be able to do the following with our car:
  * `Car.sell(newOwner)`
    * We should able to sell a car to someone, which should update the `owner` and `previousOwners` array.
    * This takes 1 string parameter for the new owner's name.
    * The old owner should be pushed to the end of the `previousOwners` array. 
    * The new `owner` should be set to the parameter passed in.
  * `Car.paint(newColor)`
    * We should be able to paint the car a new color
    * This takes 1 string parameter for the new color's name
    * This should update the color of the car to the new color.

### Phase II

Implement and test the following methods:

* `Car.start()`
  * Should change the running value of the car to `true`.
* `Car.off()`
  * Should change the running value to `false`.
* `Car.driveTo(destination)`
  * Should `console.log` `"driving to <destination>"`, but only if the car is running.
  * Should return true if it is successful and false if it is not.
* `Car.park()`
  * Only if the car is not running, you should console.log `parked!!`.
  * Should return true if it is successful and false if it is not.


### Phase III

Add the following property as a parameter to the **constructor**:

* `passengers`
  * Should be optional and default to an empty array if not specified.

Implement the following methods:

* `Car.pickUp(name)`
  * Should take a `name` and `console.log` that you are `"driving to pick up <name>"`, but only if the `car` is running AND there are enough seats available.
  * Should also update the `passengers` array to include the new passenger.
  * Should also return true on success and false on failure.
  * The newly picked up passenger should be `pushed` to the end of the array.
* `Car.dropOff(name)`
  * Should take a `name` and remove them from the `passengers` array, but only if they are in the array.
  * Should also only drop them off if the car is `on`.
  * Should also output `"driving to drop off <name>"` and return true on success and false on failure.
* `Car.passengerCount()`
  * Should return the number (integer) of passengers currently in the car.

**NOTE:** When deciding if there are enough seats available, remember that the driver takes up 1 seat, but is NOT counted as a passenger in passengerCount(). You can assume the driver is the owner.

<br>

## ES6 Classes

Once you successfully complete the phases and requirements above it's time to refactor into an ES6 Class!

Comment out the code you created above. I've provided starter code for a Car class. Start at Phase I and refactor your code into an ES6 class. The tests will work the same.

---

## Licensing
1. All content is licensed under a CC-BY-NC-SA 4.0 license.
2. All software code is licensed under GNU GPLv3. For commercial use or alternative licensing, please contact legal@ga.co.
