---
{"dg-publish":true,"permalink":"/development/obsidian/aligning-image/","dgShowToc":true,"created":"2024-12-08T16:40:52.788+01:00","updated":"2024-12-09T22:32:33.521+01:00"}
---

To align images in Obsidian, a custom CSS snippet is needed. Once it is set, this allows you to center or right-align images while scaling the image size. 

# Step 1: Create a CSS snippet

1. Navigate to the snippets folder in your Obsidian Vault. 
2. Create a new file called `Image Align.css` and add the following CSS code.

```
img[alt*="center"] {
    display: block;
    margin-left: auto;
    margin-right: auto;
}

img[alt*="right"] {
    float:right;
    clear:right;
    margin-left: 1rem;
    margin-bottom: 2px;
    margin-top: 2px;
}
```

---

# Step 2: Activate the Snippet

1. Go to **Settings** → **Appearance** 
2. Scroll down to **CSS Snippet**
3. Turn  **Image Align** in the list **ON**.


---

# Step 3: Insert an Align an Image

1. Insert an image
2. To specify alignment and sizer, modify the syntax as

`!`[`[picture name|``center``|``350``]``]`

- `center`: Centers the image.
- `right or center`: Aligns the image to the right or center.
- `100`: Scales the image to 100 pixels in width.

# Reference

https://forum.obsidian.md/t/align-image/78050