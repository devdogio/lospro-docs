# ISightTarget

## Example code

All you have to do is implement the interface in your script.
Next all methods have to be implemented. The ISightTargetCallbacks are auto. implemented, as the ISightTarget already implements this interface for you.

```csharp
public partial class SightTargetBehaviour : MonoBehaviour, ISightTarget
{
    // Interface implementation here...
}
```

Also see  [IObserverCallbacks](IObserverCallbacks.md)