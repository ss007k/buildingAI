# Similar Image Identification
Building AI course project

## Summary

Identification of similar images from a photo timeline to enable storage savings. This solution could be used in a mobile or desktop app giving the user the ability to choose the photos to retain among a set of similar looking images.

## Background

1.4 Trillion photos will be taken in 2020 as per this [forecast](https://focus.mylio.com/tech-today/how-many-photos-will-be-taken-in-2020). With the ease of taking digital photos, majority of the users take multiple photos of the same 'scene' till it looks 'best'; each of the images possibly differ only slightly in terms of point of view, composition etc.. Unfortunately, most of these similar looking photos remain, adding to storage costs both on device and offline storage costs. 

The solution intends to identify similar looking images to the user and enable them to retain the memorable shots.

## How is it used?

Given a photo timeline, where each photo has a timestamp, the solution will start by identifying a set of images shot within a user specified time interval (e.g. 1 min) and determine all similar looking images from this set. It will report the similarity as a percentage (e.g. 75% similar) between all pairs of images that are adjacent on the chosen time interval.

## Data sources and AI methods

The easiest data source for this is our own mobile photos timeline, where we have similar looking images. One possible option is to use Siamese neural networks to identify the similar looking images.

## Challenges

There could be classes of similar looking images that may not be identified by this solution. E.g. if a user shoots the same scene using different camera settings (e.g. fix over/under exposure), then the solution should still be able to identify it. Now, there could be a multitude of such scenarios, some of which may not be comprehended. 
Since this runs on device, and is entirely upto the user to invoke it's usage, there is no foreseeable ethical issue in deploying the solution.

## What next?

We need to break this into a number of smaller problems to solve:

* identify the set of images from a timeline using a user specified time interval (Python scripting)
* use AI to find the similar looking images from the above step
* (optional) wrap this into a mobile app 

## Acknowledgments

BuildingAI course
