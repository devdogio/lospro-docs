# IObserverCallbacks

For added flexibility you can receive an observer's callbacks using a single interface. Simply create a new script, implement the `IObserverCallbacks` interface and attach the component to an observer.

<iframe width="560" height="315" src="https://www.youtube.com/embed/vYYkynDsF6g" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

**Note: All Los Pro code is in the namespace Devdog.LosPro; You'll need to add the using at the top of your scripts.**

The callbacks will auto. be called by Los Pro, as long as they're attached to an observer. The observer's children won't be called, so make sure you attach the component to an observer.

```csharp
void OnTargetCameIntoRange(SightTargetInfo info);
void OnTargetWentOutOfRange(SightTargetInfo info);

void OnTargetDestroyed(SightTargetInfo info);

void OnTryingToDetectTarget(SightTargetInfo info);
void OnDetectingTarget(SightTargetInfo info);
void OnDetectedTarget(SightTargetInfo info);
void OnStopDetectingTarget(SightTargetInfo info);
void OnUnDetectedTarget(SightTargetInfo info);
```

## Example implementation

Note the added component "MyObserverCallbacks" just above the observer behaviour. Because it's on the same object it will now receive all callbacks that the ObserverBehaviour will also receive.

```csharp
using UnityEngine;
using Devdog.LosPro;

public class MyObserverCallbacks : MonoBehaviour, IObserverCallbacks
{
    public void OnTargetCameIntoRange(SightTargetInfo info)
    {
    }

    public void OnTargetWentOutOfRange(SightTargetInfo info)
    {
    }

    public void OnTargetDestroyed(SightTargetInfo info)
    {
    }

    public void OnTryingToDetectTarget(SightTargetInfo info)
    {
    }

    public void OnDetectingTarget(SightTargetInfo info)
    {
    }

    public void OnDetectedTarget(SightTargetInfo info)
    {
    }

    public void OnStopDetectingTarget(SightTargetInfo info)
    {
    }

    public void OnUnDetectedTarget(SightTargetInfo info)
    {
    }
}
```