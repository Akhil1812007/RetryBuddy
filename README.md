# RetryBuddy

**RetryBuddy** is a lightweight .NET library that helps developers handle transient failures gracefully by providing:

- **Automatic retries** for operations that may fail temporarily  
- **Delay between retries** to avoid hammering services  
- **Fluent, developer-friendly API** for both async and sync code  
- (Future) Support for **timeouts** and **fallbacks**

---

## **Problem**

Modern applications frequently call APIs, databases, or external services. Sometimes these calls fail due to:

- Network glitches  
- Temporary server overload  
- Locked files or database deadlocks  
- Other transient failures  

Without a retry mechanism, applications fail immediately, leading to poor user experience or wasted resources.

---

## **Solution**

RetryBuddy allows developers to wrap any operation with **retry logic**, automatically trying again when a failure occurs, with a configurable delay and maximum attempts.

Example use cases:  
- API requests that occasionally fail  
- Database queries that may face temporary deadlocks  
- File operations on network drives  

---

## **Installation**

You can install via NuGet (when published):

```bash
dotnet add package RetryBuddy
