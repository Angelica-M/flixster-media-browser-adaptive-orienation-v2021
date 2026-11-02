# Flixster 
Flixster is an app that allows users to browse movies from the [The Movie Database API](http://docs.themoviedb.apiary.io/#).

## Topics Demonstrated

### Media Orchestration & Hardware Integration
* **hardware-video-orchestration** — Managed hardware-accelerated media renderers to decode and play back video layers natively.
* **third-party-sdk-integration** — Programmatically embedded, configured, and lifecycle-managed the external YouTube API player runtime.
* **full-screen-rendering** — Overrode standard OS window layouts to maximize visual component frames across the entire physical display.
* **asynchronous-image-loading** — Threaded network stream downloads for image assets to prevent blocking the UI layout thread.

### Responsive Engineering & Context Transitions
* **responsive-ui-engineering** — Coded adaptive user interface layouts that dynamically adjusted spacing and components based on screen geometries.
* **layout-orientation-adaptation** — Constructed distinct portrait/landscape XML resource pathways to automatically rearrange component structures upon rotation.
* **conditional-rendering** — Swapped core image view nodes (Poster vs. Backdrop) dynamically based on the current physical aspect ratio state.
* **intent-pipeline-engineering** — Serialized and passed structured movie data payloads across isolated Android Activity component boundaries.

### Data Engineering & External API Consumption
* **rest-api-consumption** — Formulated, transmitted, and parsed HTTP network payloads from The Movie Database web services.
* **json-deserialization** — Converted incoming text-based web API responses into structured local data object matrices.
* **data-binding** — Directly mapped parsed object vectors to front-end UI view containers (TextView, RatingBar, ImageView).
* **dynamic-component-injection** — Programmatically inflated and drew numerical rating parameters directly into specialized graphic indicator nodes.

### Software Engineering & Structural Patterns
* **multi-view-architecture** — Segregated core user interactions across discrete screen boundaries (Listing Feed vs. Detailed Overview Screen).
* **view-recycling-mechanics** — Leveraged dynamic adapter architectures to efficiently handle, re-use, and render rows within memory bounds.
* **decoupled-architecture** — Separated client presentation layers entirely from the underlying asset provider web server.
* **systems-validation** — Tested structural layout transitions to ensure no state degradation occurred during configuration modifications.

### Computing Foundations & Interface Layouts
* **state-transition-governance** — Managed the exact lifecycles of parent and child views to prevent data loss during backward screen navigation.
* **mobile-architecture** — Managed activity contexts, layout lifecycle bounds, and component relationships inside a mobile OS environment.
* **object-oriented-programming** — Used class inheritance structures and modular polymorphism to build out view elements.
* **event-driven-programming** — Implemented local interface event listeners to trigger immediate screen transformations upon tactile item selections.


## Flix Part 2

### User Stories

#### REQUIRED (10pts)
- [X] (8pts) Expose details of movie (ratings using RatingBar, popularity, and synopsis) in a separate activity.
- [X] (2pts) Allow video posts to be played in full-screen using the YouTubePlayerView.

#### BONUS
- [ ] Implement a shared element transition when user clicks into the details of a movie (1 point).
- [ ] Trailers for popular movies are played automatically when the movie is selected (1 point).
  - [ ] When clicking on a popular movie (i.e. a movie voted for more than 5 stars) the video should be played immediately.
  - [ ] Less popular videos rely on the detailed page should show an image preview that can initiate playing a YouTube video.
- [ ] Add a play icon overlay to popular movies to indicate that the movie can be played (1 point).
- [ ] Apply data binding for views to help remove boilerplate code. (1 point)
- [X] Add a rounded corners for the images using the Glide transformations. (1 point)

### App Walkthough GIF

<p float="left">
<img src="https://github.com/Angelica-M/Flixster/blob/master/demoFlixster2.gif" width=250><br>
<img src="https://github.com/Angelica-M/Flixster/blob/master/demoFlixster2.1.gif" width=250><br>
</p>
<img src="https://github.com/Angelica-M/Flixster/blob/master/demoFlixster2.2.gif" width=525><br>

### Notes
 When using the YouTube v3 API, use an emulator of API Level 28 or 29 but not of Level 30. To restore the app to the state in demoFlixster2, convert line
  Glide.with(context).load(imageUrl).transform(new RoundedCornersTransformation(60, 0)).into(ivPoster); 
to 
  Glide.with(context).load(imageUrl).into(ivPoster);
of MovieAdapter.java.

## Open-source libraries used
- [Android Async HTTP](https://github.com/codepath/CPAsyncHttpClient) - Simple asynchronous HTTP requests with JSON parsing
- [Glide](https://github.com/bumptech/glide) - Image loading and caching library for Android

---

## Flixster Part 1

### User Stories

#### REQUIRED (10pts)
- [X] (10pts) User can view a list of movies (title, poster image, and overview) currently playing in theaters from the Movie Database API.

#### BONUS
- [X] (2pts) Views should be responsive for both landscape/portrait mode.
   - [X] (1pt) In portrait mode, the poster image, title, and movie overview is shown.
   - [X] (1pt) In landscape mode, the rotated alternate layout should use the backdrop image instead and show the title and movie overview to the right of it.
- [ ] (2pts) Display a nice default [placeholder graphic](https://guides.codepath.org/android/Displaying-Images-with-the-Glide-Library#advanced-usage) for each image during loading
- [ ] (2pts) Improved the user interface by experimenting with styling and coloring.
- [ ] (2pts) For popular movies (i.e. a movie voted for more than 5 stars), the full backdrop image is displayed. Otherwise, a poster image, the movie title, and overview is listed. Use Heterogenous RecyclerViews and use different ViewHolder layout files for popular movies and less popular ones.

### App Walkthough GIF
<img src="https://github.com/Angelica-M/Flixster/blob/master/demoFlixster.gif" width=250><br>

### Notes
No challenges were faced.

### Open-source libraries used
- [Android Async HTTP](https://github.com/codepath/CPAsyncHttpClient) - Simple asynchronous HTTP requests with JSON parsing
- [Glide](https://github.com/bumptech/glide) - Image loading and caching library for Androids
