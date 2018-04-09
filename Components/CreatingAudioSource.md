# Creating Audio Source

Audio sources can be created at through a simple API.

## Code example

```csharp
var audioSource = AudioSourceManager.CreateAudioSourcePooled(Vector3.zero, emitter); // where emitter is the object that is emitting the sound (can be null).
audioSource.Emit(); // Call Emit() when you're ready to emit the sound.

// And for 2D
var audioSource2D = AudioSourceManager2D.CreateAudioSourcePooled(Vector3.zero, emitter); // where emitter is the object that is emitting the sound (can be null).
audioSource2D.Emit(); // Call Emit() when you're ready to emit the sound.
```

## Code example (complex)

When using your own implementation of `IAudioSource` you can use the generic method to get a new object. **Note, these are not pooled.**

```csharp
var audioSource = AudioSourceManager.CreateAudioSourceNotPooled(Vector3.zero, emitter); // Type T has to inherit the IAudioSource interface.
audioSource.Emit();

// And for 2D
var audioSource = AudioSourceManager2D.CreateAudioSourceNotPooled(Vector3.zero, emitter); // Type T has to inherit the IAudioSource interface.
audioSource.Emit();
```