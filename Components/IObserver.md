# IObserver

Observers are used to detect targets and are the wrappers for `ISight`. The observers receive all callbacks.

## Example code

All you have to do is implement the interface in your script. Next all methods have to be implemented. The IObserverCallbacks are auto. implemented, as the IObserver already implements this interface for you.

```csharp
public partial class ObserverBehaviour : MonoBehaviour, IObserver
{
    // Interface implementation here...
}
```

Also see  [IObserverCallbacks](IObserverCallbacks.md)