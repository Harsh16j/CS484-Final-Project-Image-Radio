# CS 484 Project - Image Radio

## Group Members:

1. Jason James Dsouza (UIN: 677667371)
2. Anjani Sruti Doradla (UIN: 670111749)
3. Harsh Jethwani (UIN: 670509818)

## Link to hosted app

https://image-radio-ai.netlify.app/<br/>

<b>Link to App's Screencast showing Final functionality in action:</b> https://drive.google.com/file/d/1z26fc4TEsQXv54e9EIx7PjdzC85vuLZG/view?usp=sharing

<b>Link to App's Screencast showing MVP functionality in action:</b> https://drive.google.com/file/d/1kkrAsscLu3QhdpBbjFRY44xYlZltSqDm/view?usp=share_link

<b>Note:</b> The Spotify Web SDK requires you to have Spotify Premium to use the Player in our application. Since the image generation DALLE-2 API has a fixed credit limit, we are limiting the 'Add a song to the radio' feature only to admin users, to avoid exhausting our API calls. Anyone with a Spotify Premium Account can view and play the songs (with synchronized lyrics and AI generated images) on our application. However, only admin users can add a new song to it.

## Architecture Diagram

![Alt text](public/images/Architecture_Diagram.png "Architecture Diagram")

## Features

-   OAuth with Spotify
-   Spotify Web Player (with audio casting between connected devices)
-   Request to add a song to the playlist (for admin users only)
-   Resume progress to add a song to the playlist in case of an interruption
-   Song playlist fetched from the database
-   AI generated images using song lyrics (also stored in the database)
-   Synchronized lyrics with song audio
-   Synchronized AI generated images with song audio

## What does your application do?

Our application aims to emulate a radio station, which uses the lyrics of a song of the user's choice, to generate a series of images, and synchronizes the music audio with its respective images.

## What makes it different than a CRUD app? I.e., what functionality does it provide that is not just a user interface layer on top of a database of user information, and the ability to view / add to / change that information?

Our application uses the Spotify API to fetch the timestamped lyrics of a given song with its annotations, after which it displays a series of AI generated images based on the lyrics, and plays its synchronized audio.

## What security and privacy concerns do you expect you (as developers) or your users to have with this application?

Currently, we plan to implement Spotify OAuth to access the user's playlists. Here, the user may be concerned about their private data getting compromised. However, we will ensure to use the correct authorization scope when implementing OAuth, so that we only get the specific user data that our application requires.

## MVP Desciption

We plan to play a song and its lyrics, in a synchronous manner. We will use <b>OAuth with Spotify</b> for user login. After this, we will fetch the timestamped lyrics of the song and play it using the <b>Spotify API</b>. <b>Supabase</b> database will be used for the backend, while <b>React</b> will be used for the frontend. We will use <b>GitHub</b> for version control along with <b>Netlify</b> for CI and hosting. We successfully completed all the planned tasks for the MVP.

## Final Submission Description

We plan to play a song and display AI generated images from its lyrics, in a synchronous manner. We will use <b>OAuth with Spotify</b> for user login. After this, we will fetch the timestamped lyrics of the song and play it using the <b>Spotify API</b>. <b>Supabase</b> database will be used for the backend, while <b>React</b> will be used for the frontend. We will use <b>GitHub</b> for version control along with <b>Netlify</b> for CI and hosting. Our project also utilizes the newly released <b>DALLE-2 API</b>, to generate images based on the lyrics of the song. We successfully completed all the planned tasks for the final submission.
