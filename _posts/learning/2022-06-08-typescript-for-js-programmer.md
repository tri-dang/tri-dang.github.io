---
layout: post
title: typescript-for-js-programmer
categories: [engineering]
tags: [learning]
date: 2022-06-08 11:39 +0700
locale: en
---
- [Engineering] [Typescript for JS Programmer](https://www.typescriptlang.org/docs/handbook/typescript-in-5-minutes.html)
  + Type by Inference: TS will define type of a variable by assigned value
  + Interfaces vs Types: using interface to define type
  + Unions: a variable can have multiple types
    ```
      function getLength(obj: string | string[])
    ```
  + Generics: can use Type as generic Type and assign a specific type to Type in
    declare
    ```
      interface Container<Type> {
        push: (obj: Type) => void;
        pop: () => Type;
      }

      declare const stringContainer: Container<string>;
      stringContainer.push("abc");
    ```
  + Duck Typing = Structural Typing = shape-matching:
    ```
      interface Point {
        x: number;
        y: number;
      }

      const point = { x: 1, y: 2 }; // auto match to Point type
      const rect = { x: 1, y: 2, width: 10, height: 30 }; // auto match to Point type (kind of casting to Point)
      const color = { hex: "#FFFFFF" }; // failed-matched to Point type
    ```
