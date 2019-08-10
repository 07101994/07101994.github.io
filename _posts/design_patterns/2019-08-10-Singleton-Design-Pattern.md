---
layout: post
title: Singleton Design Pattern
---

Singleton design pattern makes sure that there should be only one instance of the specific class at a given time. Please refer below example code for C# example.

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
