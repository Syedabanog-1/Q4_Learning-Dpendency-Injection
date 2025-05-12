# Q4_Learning-Dpendency-Injection

✅ What is Dependency Injection (DI)?
Dependency Injection (DI) is a design pattern where an object or function receives its dependencies from an external source, rather than creating them internally.

In simple terms:

Instead of a function or class creating the things it needs (like database connections, services, etc.), these are provided (injected) from outside.

🎯 Why use Dependency Injection?

Loose coupling: Your components are not tightly bound to each other.

Reusability: You can reuse dependencies in multiple places.

Easy testing: You can easily mock dependencies in your tests.

Cleaner code: Separation of concerns (logic and dependencies are separate).

✅ Dependency Injection in FastAPI

In FastAPI, you use the Depends function to inject dependencies automatically.

FastAPI will:

Resolve the dependency when the route is called.

Automatically handle parameters (query, path, headers, etc.).

Handle exceptions, validation, and reusable logic.

🔧 Example:


from fastapi import FastAPI, Depends

app = FastAPI()

# Dependency function

def get_database_connection():
    return "Database Connection"

# Injecting dependency in route

@app.get("/items/")
def read_items(db_connection = Depends(get_database_connection)):
    return {"db": db_connection}
Here:
The route doesn't create the database connection itself.

It gets it from the get_database_connection() function.

FastAPI manages the lifecycle and injection.

✅ Benefits of Dependency Injection


Loose Coupling:	Components are independent of each other
Easy Testing:	Dependencies can be easily mocked or replaced
Reusability:	Use the same dependency in multiple places
Clean and Maintainable Code:	Separates business logic from dependency creation

Example Real-life analogy:

Imagine you are using an electric socket (dependency) to power your fan (application logic).

The fan doesn't generate its own electricity.

It receives power from the socket (dependency injection).

This makes the fan simpler, reusable anywhere, and easy to test by just plugging it in.
************************************************************************************************************************
------------------------------------------------------------------------------------------------------------------------
************************************************************************************************************************



![Application Startup Complete](https://github.com/user-attachments/assets/7c4f02c4-00db-42e7-9a29-505476af3742)

# URL EXAMPLES

1. With Root

   ![dependency-Root (slash)](https://github.com/user-attachments/assets/2d2f40bf-f773-404e-92aa-cbeb42f21ff5)

2.Simple Dependency

![simple-dependency](https://github.com/user-attachments/assets/c1e6570e-6a75-4cf2-8068-60b762602aae)

3. Dependency With Parameters

   ![dependency-with-parameter](https://github.com/user-attachments/assets/35b150f8-31c5-44f0-a06e-8ebf4e8bf796)

  4.  Dependency with Query Parameters For Login

     ![dependency-with-queury-parameter](https://github.com/user-attachments/assets/422820ad-a7d0-4813-b6e9-bc61692e8f8f)

     5.Dependency with Query Parameters With Wrong Credentials

![dependency-with-queury-parameter-wrongCredentials](https://github.com/user-attachments/assets/544f8afb-7ebf-422e-a2ae-fa34f6d34a78)

5.Multiple Dependencies with Path Parameter

![multiple-dependencies-with-path-parameter](https://github.com/user-attachments/assets/561e1f97-0468-4a93-aacc-91907168f136)

6.Get Blog by ID (404 If Wwrong ID)

![get-blog-by-id](https://github.com/user-attachments/assets/80654dcd-322b-460c-a8d7-6cb38a16d101)

7.Get User by ID (404 If Wrong ID)

![get-user-by-id](https://github.com/user-attachments/assets/dc0c1720-dfeb-47d9-9efa-da7737fa6739)

8.Fastapi Documents(Bonus)

![fastapi url-path-doc](https://github.com/user-attachments/assets/ce7c7141-e07d-466a-9ccb-abaf7e9054d6)











