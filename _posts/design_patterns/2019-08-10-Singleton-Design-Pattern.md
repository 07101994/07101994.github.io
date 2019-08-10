---
layout: post
title: Singleton Design Pattern
---

## Problem it solves

Singleton design pattern makes sure that there should be only one instance of the specific class at a given time.

## Example

```csharp
// Singleton class Customer
public class Customer
{
    private static readonly Lazy<Customer> _lazy = new Lazy<Customer>(() => new Customer());

    private Customer() { }

    public static Customer Instance
    {
        get
        {
            return _lazy.Value;
        }
    }
}
```
