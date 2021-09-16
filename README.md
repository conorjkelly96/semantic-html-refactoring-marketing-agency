# Marketing Agency Website: Semantic Refactoring

## About the project

The exercise undertaken in this repository was to refactor the HTML and CSS code previously used to build the 'Horiseon' website. The original version lacked the use of semantic elements within the HTML code, likewise the CSS required some simplification by removing duplicates and restructuring some of the original HTML class structure to ensure a concise and clean solution. The goal of this exercise is to ensure Horiseon's website is optimized for search engines and increases accessibility.

## Original Website

Below is a screenshot from the original website prior to refactoring.

![Original Website](assets/images/01-html-css-git-homework-demo.png)

## Technologies Used

- HTML
- CSS

## Solution Overview

### HTML Code Refactoring

The original Horiseon website contained no semantic HTML syntax. Firstly, I restructured the HTML code to contain more semantic syntax.

The code below is an example of the original source code:

```
<div class="header">
      <h1>Hori<span class="seo">seo</span>n</h1>
      <div>
        <ul>
          <li>
            <a href="#search-engine-optimization">Search Engine Optimization</a>
          </li>
          <li>
            <a href="#online-reputation-management"
              >Online Reputation Management</a
            >
          </li>
          <li>
            <a href="#social-media-marketing">Social Media Marketing</a>
          </li>
        </ul>
      </div>
    </div>
```

This code was refactored to contain `<header>` and `<nav>` tags to give the document better semantic structure:

```
<header class="navbar">
      <h1>Hori<span class="seo">seo</span>n</h1>
      <!-- navbar containing links -->
      <nav>
        <ul>
          <li>
            <a href="#search-engine-optimization">Search Engine Optimization</a>
          </li>
          <li>
            <a href="#online-reputation-management"
              >Online Reputation Management</a
            >
          </li>
          <li>
            <a href="#social-media-marketing">Social Media Marketing</a>
          </li>
        </ul>
      </nav>
    </header>
```

### CSS Code Refactoring

I found the original CSS code contained duplicate blocks of formatting targeting similar blocks, and found an opportunity to reduce complexity through class commonality. An example below represents the original source code:

```
.benefit-lead {
  margin-bottom: 32px;
  color: #ffffff;
}

.benefit-brand {
  margin-bottom: 32px;
  color: #ffffff;
}

.benefit-cost {
  margin-bottom: 32px;
  color: #ffffff;
}
```

Which was refactored to a single class within the HTML code and updated within the CSS code:

```
/* class commonality to alleviate need to duplicate CSS blocks */
.benefit-subsection {
  margin-bottom: 32px;
  color: #ffffff;
}
```

## Final Website Structure

The layout of Horiseon's website after refactoring the CSS and HTML source code is shown below:

![Original Website](assets/images/01-html-css-git-homework-demo.png)

Note, the layout and aesthetic design of the website has not changed. It's kept it's original layout, however the source code has been semantically refactored and improved to ensure improved Search Engine Optimization and accessibility.

## To Do

In the future, I will update this website to include media queries, ensuring the website is fit for users across different viewports.
