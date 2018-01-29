# Ci.Retry
A support method for easy retry logic.

## Notice
**This is not my wrting code**
<br/>
This library is implement a stackoverflow question's answer, it's very good and clean way
<br/>
I implement answer to a nuget package for easy use
<br/>

**[https://stackoverflow.com/a/1563234/1799047](https://stackoverflow.com/a/1563234/1799047)**

## Usage
install nuget package
```
Install-Package Ci.Retry
```

then at want to retry method use:
```csharp
Retry.Do(() => SomeFunctionThatCanFail(), TimeSpan.FromSeconds(1));
```
or:
```csharp
Retry.Do(SomeFunctionThatCanFail, TimeSpan.FromSeconds(1));
```
or:
```csharp
int result = Retry.Do(SomeFunctionWhichReturnsInt, TimeSpan.FromSeconds(1), /*Attempt Count*/ 4);
```
