# Pilar Framework and gogen tools

## PILAR (Progressive, Intuitive Layered Architecture)

### Written based on Clean Architecture and Domain Driven Design

Basically This Architecture is written based on clean architecture (https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html). In this case, PILAR already do some modification to the architecture like more a code layout and folder structure.

## GOGEN as Helper tools to generate PILAR Framework

Currently GOGEN is the only tools which apply PILAR in golang programming language. GOGEN can help the programmer to generate boiler plate code based on PILAR architecture

## domain

Domain defined based on domain driven design bounded context

- https://martinfowler.com/bliki/BoundedContext.html

## usecase

The basic concept comes from clean architecture but the detail one is added by PILAR

### inport

- inport is interface that has one method with name Execute with one params input and one return value
- inport request define all required payload to run the usecase
- inport response define all response after run the usecase

### interactor

- has a struct which implement inport interface
- has a constructor that receive one Outport
- interactor is the place where we define the core of business process
- it use the entity, value object, repository and service to solve the usecase problem
- it can have many interactor as alternative algorithm but only one is used

### outport

- outport is an interface that provide any required data or action that needed by Interactor to run the usecase
- outport commonly compose other interface from repository and service
- outport is a contract (that need to be fulfiled) for anyone who want to run the usecase

---

## model

The basic concept comes from domain driven design and the detail one is added by PILAR

### entity

### value object

### service

### repository

### enum

Added by PILAR

### errorenum

Added by PILAR

---

## gateway

Named based on clean architecture gateways

### implement outport interface

### use struct composition

### panic in contructor

---

## controller

The detail concept is added by PILAR

### handler

each handler handle one use case. But there is a case where one handler may handle multi usecase at once

### interceptor

### router

---

## application

### binding controller, usecase and gateway

---

## shared model

## shared infrastructure
