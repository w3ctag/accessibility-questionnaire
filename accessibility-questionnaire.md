# W3C TAG Accessibility Questionnaire

This document is intended to ne used in the context of the [TAG Review](https://tag.w3.org/workmode/) process. 

This checklist is a quick mechanism to assess whether or not your proposed design should go through a detailed accessibility review.  If you answer YES to any of the questions below, you should seek advice from relevant domain experts. 

Note that this checklist doesn’t constitute an accessibility self-review, only a way to determine whether a more thorough review might be required.

1. Does the design being proposed add anything to the user interface? (YES/NO) For example:

   * a new type of UI element
   * a new mechanism for drawing custom user interfaces
   * a requirement for some user agent UI

Why? Visible interface components must be carefully designed to ensure they are flexible enough to work in a wide range of contexts, for example, when users require extremely large fonts or access the web using assistive technologies such as screen readers.

2. If you answered YES to question 1, is the interface only available for a given amount of time? (YES/NO/NA) For example:

   * a notification that disappears 

Why? There are a range of reasons why a time-limited visual interface may cause problems for users; for example, screen reader users may not be aware that the interface is available (or else struggle with too many interruptions), or users may not be able to reach the interface in time to interact with it before it disappears. 

3. Does the design being proposed add anything audible to the user interface? (YES/NO) For example:

   * a notification sound
   * a speech-based interface
   * an audio stream (alone or with other timed media).

Why? Audio cues may not always be accessible to users due to disability or because the use of audio is not appropriate for them. Depending on the purpose of the audio, it may be appropriate to provide mechanisms to provide alternative forms for the same information, to provide a redundant visual cue, or allow configuration options.

4. Is any user-presented data passed through a protocol if the spec is API-only? (YES/NO) For example:

   * a transport mechanism for media, such as images, video, or user strings, which may benefit from including an alternative representation as part of the payload

Why? Any given media type in isolation (for example, speech) may be inaccessible or inappropriate for a certain subset of users, so authors should be able to provide alternative forms. For example, if a protocol has a way to transmit images, it should also be able to present an accompanying image description string, either in the same payload or through an auxiliary mechanism if the description is context-sensitive. (For example, the alt attribute in an <img> element is auxiliary because image descriptions are very context-dependent.) 

5. Does the specification change how user input is interpreted at an API level? (YES/NO) For example:

   * a new type of input event
   * a change to an existing mechanism for handling user input (e.g., focus)

Why? For users of assistive technology, user input is often done by the assistive tool. This requires the tool to be able to determine the type of input needed and, when it is needed, to present an appropriate affordance to the user. New ways to provide user input will require consideration to ensure assistive technologies will be able to handle them appropriately.

6. Does the specification concern user input, potentially constrained to a specific device or modality? (YES/NO) For example:

   * an API limited to a particular device such as a gamepad, touch screen, or pen
   * a requirement for a user to perform a specific type of interaction in order to enable some aspect of the API (e.g., User Activation dependent)

Why? Specific devices may have unique accessibility considerations, and limiting technology to a particular device may unnecessarily exclude users if a more general design could be created instead.

7. If you answered YES to any of the above questions, does the specification provide authoring advice? (YES/NO) For example:

   * example code
   * guidance on best practices

Why? Authoring advice should be given in a way that allows authors to write content that is accessible to users and take advantage of relevant features in the API. 
