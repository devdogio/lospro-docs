# Listener

The listener is used to detect any audio sources in the scene.

<iframe width="560" height="315" src="https://www.youtube.com/embed/2M5jJKCYNkE" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

-   **Raycast layer:** The layers used to verify if the audio source can be heard. Optionally custom hearing validators can be implemented.
-   **Min hearing volume:** The minimal volume the audio has to have in order to hear the source. Volume is calculated based on the normalized distance. (1 at the center of the audio source, 0 at the outer edge).
-   **Debug:** When debug is enabled messages will be logged to the Unity console.