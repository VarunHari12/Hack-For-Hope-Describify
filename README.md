# Goals
When first starting this project, we wanted to create an app that functioned as a set of “supercharged eyes” for those who are visually impaired. All we wanted to do in the beginning was to allow users to scan objects and receive vivid descriptions of those objects so that they could better visualize them in their head. After working on the project, we realized that there was so much more we could do and started making additional custom modes to help the visually impaired with daily tasks such as cooking or shopping. Overall, we surpassed our initial expectations for the project, and we are very happy with the result.

# What it does
**Describify** empowers the visually impaired to perform daily tasks with greater ease.

Describify has four modes: **Shopping**, **Description**, **Text**, and **Recipe** mode. The description mode lets a user scan an object, receiving a vivid, insightful description in return. This can help visually impaired people to better visualize objects and fully understand what they're "looking" at.

The shopping mode lets the user scan any product, receiving the product name and price as a result. Those who are visually impaired can put this to good use while shopping to identify brands, products, sizes, etc.

Text mode allows users to identify any written text, regardless of language, and have Describify speak it to them in English. This can be especially useful in public spaces that don't have text accompanied by braille. This mode could also be used to read something like a map to help the user navigate a public space.

Recipe mode allows users to scan ingredients that they have available, then, Describify will provide them with possible dishes they can make with the ingredients, as well as the recipe for one of the dishes. An example use case of this mode could be a user scanning their refrigerator to see what ingredients they have and what dishes they can make.

Describify provides text-to-speech output for all responses, ensuring a more understandable and easy experience for the visually impaired. We have optimized the TTS output to make sure the content of the speech sounds as natural as possible when speaking.

# How we built it
The GUI for Describify was made using the Tkinter library for Python. For image capturing, we used OpenCV to capture frames from the camera as well as identify common objects. The identified object is then put through an AI object detection model which sends back a response that is custom to whatever mode the user is in. Throughout the project, we used OpenAI text-to-speech and visual recognition models to provide an understandable, accurate, and thorough experience for the user. We designed image detection to work even in blurry, low-quality, and low-light conditions to help a visually impaired person even if they can’t fully recognize what they are scanning. This assures that we can always provide a satisfactory response for our users.

# Challenges we ran into
We were not able to create this application for mobile, which was our intended use case, because we didn’t have the necessary tooling (a Mac and Xcode) to create mobile apps. As a workaround, we made it possible to use your phone as a camera. We wanted to make this on mobile because we wanted the app to be touch and audio-based. This would make the GUI easy to navigate for our visually impaired users. Unfortunately, until we have the necessary tools, the project will only be usable on desktop.

We also had issues getting our AI visual recognition to understand what object we were trying to focus on. To solve this, we used OpenCV to detect the common object closest to the center of the camera and create a bounding box around that object. We could then send only the content inside the bounding box (which encompasses the object) to the AI visual recognition. This helped with accuracy tremendously, making sure the AI model was only focusing on what we wanted it to describe. It also helped make the loading speed of the response a little bit faster.

# Accomplishments that we are proud of
We are proud of learning new skills such as using Tkinter for our GUI, which we’ve never used before. We are also proud of being able to incorporate existing skills, like making requests to OpenAI models, into a real project that impacts the way people live.

# What we learned
We learned how to use OpenCV to improve object recognition, and we learned how to engineer AI model prompts to return a thoughtful output in a consistent format every time for the user. We also learned how to format text before a text-to-speech model, to improve the "human" factor of the voice output. For this project, we had to learn how to utilize the OpenCV package for object recognition. We also needed to learn how to structure AI prompts to receive thoughtful and consistent output that sounds natural when spoken aloud. These skills allowed us to enhance our project and make sure that the experience for our users was consistently good.

# What's next for Describify
We want to be able to develop this as a phone app, making it fully portable and not reliant on a computer. Describify was initially intended to be a mobile app, but because we don’t have a Mac or Xcode, we weren’t able to create it as a mobile app, and we had to develop it as a desktop app. We would also like to add more features and modes to Describify to continually improve user experience.
