---
title: "Wonders of the `tap`"
author: Danilo Hoffmann
mail: dhhyi@aol.com
bio: Danilo works as a Software Developer for the e-commerce company ... TODO 
published: 2020-01-08
last-change: 2020-01-08
keywords:
  - Angular
  - RxJS
  - Reactive Programming
  - Observables
language: en
thumbnail: tap-scenarios-header.jpg

---

**TODO**

# Introduction

- `tap` is mysterious
  - leave the stream while everything else is following the flow
  - code smell?
  - `do` was deprecated after all?!

## Scenario #1

- component property assigned as tap while subscription is somewhere else
  - -> properly subscribe?
  - -> do it as a stream altogether?
  - -> split stream + `shareReplay` and properly subscribe?

## Scenario #2

- tap for dispatching actions in facades
- tap for triggering stuff for 3rd-party integrations


## Scenario #3

- tap for triggering routing in NgRx Effects
  - ignoring the Promise?!
  - theoretical analysis: queues (micro task)
  - talk about scheduling issues:
    - ignoring Promise means routing is happening after the effect
      - can be shown with testing (fakeAsync necessary)
    - including promise follows modelled flow
      - testing: subscribe effect and check location

