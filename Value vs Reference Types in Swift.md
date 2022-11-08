Value Types vs Reference Types, and When to Use Each

In Swift there are two categories of types: value types and reference types. A value type instance keeps a unique copy of its data, for example, a struct or an enum. A reference type, shares a single copy of its data, and the type is usually a class.

Value Types vs Reference Types

Value Types
A value type instance is an independent instance and holds its data in its own memory allocation. There are a few different value types: struct, enum, and tuple.

When to Use Value Types
Use value types when comparing instance data with == makes sense. == checks if every property of the two instances is the same. With value types you always get a unique, copied instance, and you can be sure that no other part of your app is changing the data under the hood. This is especially helpful in multi-threaded environments where a different thread could alter your data. Use a value type when you want copies to have an independent state, and the data will be used in code across multiple threads. In Swift, Array, String, and Dictionary are all value types.

Reference Types
In Swift, reference type instances share a single copy of their data, so that every new instance will point to the same address in memory. A typical example is a class, function, or closure.

When to Use Reference Types
Use a reference type when comparing instance identity with === makes sense. === checks if two objects share the same memory address.
They’re also useful when you want to create a shared, mutable state. As a general rule, start by creating your instance as an enum, then move to a struct if you need more customization, and finally move to class when needed.


LucidChart link: https://lucid.app/lucidchart/0f0d4748-cecb-4734-bfdc-330de5ec7fc2/edit?viewport_loc=-416%2C62%2C2535%2C1426%2C0_0&invitationId=inv_c527567d-7cbd-4ebb-bdca-fb516fb3494d
