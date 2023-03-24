# Horiseon Market Research Page

## Description

The goal was to refactor the given code, aiming for accessiblity and clarity.

I learned about the many different considerations for alt text and how a screen reader interprets differently written code.

## Installation

Here is a link to my GitHub Pages site: https://benstorlie.github.io/horiseon/

## Usage

Here is a screenshot of the webpage.

![Here is a screenshot](./assets/images/website-screenshot.png)

## Comments about my Choices
Here are some specific decisions I made, and the reasoning behind them.  I don't want someone to think that these choices were arbitrary or that I overlooked something thoughtlessly.  The following mostly came from notes to myself, so it might not be compelete.

1. Alt text
    - I found a lot of interesting guidelines for how to write alt tags depending on the purpose of the image.  I found that the images included in this page either fall into the gray zone between [decorative][1] and [informative][2], or they are definitely decorative.
    - I thought that this article was interesting: ["When can a web author use null alt text"][3]. It discusses why or why not someone would opt for null text, depending on the purpose of the image.  Ultimately, it is up to the author.
    - Icons
        - I decided that the icons were definitely in the decorative category.  Their purpose is "eye candy" to separate and emphasize the headings in the right section.
    - Large Background Image
        - My choice, for simplicity's sake, and to ensure the image behaves the same as it did originally, was to add `role=img` and an `aria-label` to the `div`.
        - The large image is styled as a background to an otherwise empty `div`.  So it is not really *behind* anything, as a background would be.
        - This article, ["Alternate text for background images: Considerations and techniques"][4], was useful, and the takeaway was:

        > - Try not to use CSS for important informational images.
        > - For ambient images that are CSS, it is a courtesy to provide alternate text. When doing so, place image in its own empty `<span>` with an `aria-label` and `role="img"`.This is also true, in a situation where CSS must be used for information content.

        - Is it really a "background" image?  There's nothing in front of it.  What is it backgrounding?  Maybe it's just a foreground image.  (I'm no graphic designer.)
        - This image definitely fits in the gray "decorative or ambient?" category.
    - The three other images
        - Similar to the background image, these also are in the gray zone.
        - One could decide that these are "eye-candy," since they are kind of redundant to the headings.
        - I'm going to make the same decision I as I did for the background image.  Just a concise, low-detail alt text is necessary.
2. Headings
    - The headings on the right are a smaller font size than the ones on the left.  However, since they aren't *sub*-headings, I'm going to promote them to `<h2>`.





[1]: https://www.w3.org/WAI/tutorials/images/decorative/#image-used-for-ambiance-eye-candy "Decorative Images"
[2]: https://www.w3.org/WAI/tutorials/images/informative/#example-4-images-conveying-an-impression-or-emotion "Informative Images"
[3]: https://www.davidmacd.com/blog/what-is-pure-decoration-alt-text-in-wcag.html "What is pure decoration alt text?"
[4]: http://www.davidmacd.com/blog/alternate-text-for-css-background-images.html "Alternate text for css background images"