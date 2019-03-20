footer: kimschles
slidenumbers: true

![inline](https://res.cloudinary.com/kimschlesinger/image/upload/v1552522996/logo-white.png)

---
![left 75%](http://res.cloudinary.com/kimschlesinger/image/upload/c_scale,w_2960/v1524009870/kimschlesinger-headshot.jpg)

# Kim Schlesinger
### Ops, Education & Software 

--- 
![inline](./images/RO-Logo-White.svg)

--- 


![inline](https://pbs.twimg.com/media/DzdauLfUcAITSMd.jpg:large)

--- 


![inline](https://res.cloudinary.com/kimschlesinger/image/upload/v1552522996/logo-white.png)

---

# Refactoring hirediversity.us

--- 
# The Journey 

![left](images/path.jpg)

^ Company is ~2 years old 
Platform is pushed out quickly with lots of developers 
Corners were cut 
I'm leaving at the end of the month 

---
## I thought I knew more than I did... 

![inline](https://media.giphy.com/media/321HrzkqKyUt6cxCOI/giphy.gif)

^ I have a master's degree in special education, I taught special education and worked with students who used assistive technology, I get the a11y newsletter and I've been to the Front Range Accessibility and Inclusive Design Meetup

--- 
![inline](https://cdn-images-1.medium.com/max/1200/1*eAP4oWRbmQh05pwNwtv0gw.png)

--- 
# What is accessibilty? 

> Web accessibility means that websites, tools, and technologies are designed and developed so that people with disabilities can use them. 

--WC3 Web Accessibility Initiative


---
# Accessibility Lessons 
1. Use multiple tools to identify issues 
1. Commit to accessibility being an ongoing process, not a one time fix
1. An accessibility refactor may be more valuable than a code refactor  

--- 

## 1. Use multiple tools to identify accessibility issues 

---
## 1. Use multiple tools to identify accessibility issues 

* WAVE Extension 
* [A11y Checklist](https://a11yproject.com/checklist)
* Good examples you can deconstruct 
* Manual Testing with a Screen Reader 

---
## WAVE Extension 

![inline](https://youtu.be/ZInUExMcVVA)

--- 
## alt text 

--- 
# Before 

```javascript
const CompanyProfileCard = (props : Props) => (
  <CustomCard onClick={props.onClick}>
      <Media left>
        <Link to={`/company/${props.id}`}>
          <Media object src={props.logo} width="100" alt="Logo"/>
        </Link>
      </Media>
```

---
# Before 

[.code-highlight: 5]

```javascript
const CompanyProfileCard = (props : Props) => (
  <CustomCard onClick={props.onClick}>
      <Media left>
        <Link to={`/company/${props.id}`}>
          <Media object src={props.logo} width="100" alt="Logo"/>
        </Link>
      </Media>
```

---
# After 

[.code-highlight: 5]

```javascript
const CompanyProfileCard = (props : Props) => (
  <CustomCard onClick={props.onClick}>
      <Media left>
        <Link to={`/company/${props.id}`}>
          <Media object src={props.logo} width="100" alt={`${props.name} logo`}/>
        </Link>
      </Media>
```
---

![left 25%](https://www.goodfreephotos.com/albums/vector-images/colorful-brain-map-vector-clipart.png)

Use JS template literals to dynamically populate alt text for images 

---

## 1. Use multiple tools to identify accessibility issues 

---
## 1. Use multiple tools to identify accessibility issues 

* [A11y Checklist](https://a11yproject.com/checklist)
* Good examples you can deconstruct 
    * [The A11y Project](https://a11yproject.com/)
    * [Eric Bailey Design](https://ericwbailey.design/writing/2019-03-05-fighting-uphill.html)
    * [Inclusive Design Principles](https://inclusivedesignprinciples.org/)
* Manual Testing with a Screen Reader 

---

# Provide a “Skip to main content” link 

---

### Add the skip nav code, or component, to the top of your header 


---

```js
import React from 'react';

const SkipNav = () => (
    <ul id="section-skipnav" aria-label="Skipnav" role="navigation">
        <li className="skipnav-item">
            <a href="#section-main">Skip to Main Content</a>
        </li>
        <li class="skipnav-item">
            <a href="/accessibility-statement">Accessibility Statement</a>
        </li>
    </ul>
);

export default SkipNav;
``` 

---

![left 25%](https://www.goodfreephotos.com/albums/vector-images/colorful-brain-map-vector-clipart.png)

Create a way for people using screen readers to skip to the main content of the page 

 ```html
<a href="#main">Skip to main content</a>
<main id="section-main">
```

--- 
# 1. Use multiple tools to identify issues 

--- 
## 2. Commit to accessibility being an ongoing process, not a one time fix

---
# Accessibility Statement 



--- 

What Can You Do? 


Company? Ask what you're doing 
School? Ask when that is covered, and if not why 
* offer lesson
Attend the FRA meetup in Boulder 



---
# Accessibility Resources
* [Wave Web Accessibility Evaluation System](http://wave.webaim.org/)
* [a11y Web Accessibility Checklist](https://a11yproject.com/checklist)
* [Inclusive Design Principles](https://inclusivedesignprinciples.org/)
* [Eric Bailey: Fighting Uphill](https://ericwbailey.design/writing/2019-03-05-fighting-uphill.html)
* [Crystal's dvlp dnvr Talk]()

--- 
# Questions


--- 
![left](https://media.giphy.com/media/5ArJanyCfxgiY/giphy.gif)

# Contact Me

**kimschlesinger.com**
**developdenver.org** 
**hirediversity.us** 

@kimschles 
on twitter, github and twitch

