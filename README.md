<div align="center">
  <img height="150" src="https://media.giphy.com/media/M9gbBd9nbDrOTu1Mqx/giphy.gif" />
</div>

<div align="center">
  <a href="https://www.linkedin.com/in/prathmesh-bavge" target="_blank">
    <img src="https://img.shields.io/static/v1?message=LinkedIn&logo=linkedin&color=0077B5&style=for-the-badge" height="25" alt="LinkedIn" />
  </a>

  <a href="https://twitter.com/PrathmB2005" target="_blank">
    <img src="https://img.shields.io/static/v1?message=Twitter&logo=twitter&color=1DA1F2&style=for-the-badge" height="25" alt="Twitter" />
  </a>
</div>

---

<br />

<h1 align="center">Hey there, I’m Prathmesh Bavge 👋</h1>

---

## 👩‍💻 About Me
I’m a **Third-year Information Technology student** at Pune Institute of Computer Technology, Pune, India.  
- 🌱 **Learning:** Next.js, Three.js, advanced React patterns, and scalable backend architectures with Python Flask.  
- ⚡ **In my free time:** I enjoy competitive programming, reading tech blogs, and scripting YouTube Shorts.

---

## 🛠 Languages & Tools
<div align="left">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" height="40" alt="JavaScript" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg" height="40" alt="TypeScript" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" height="40" alt="Python" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg" height="40" alt="Java" />
  <br/><br/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original-wordmark.svg" height="40" alt="React" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nextjs/nextjs-original.svg" height="40" alt="Next.js" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/threejs/threejs-original.svg" height="40" alt="Three.js" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/flask/flask-original-wordmark.svg" height="40" alt="Flask" />
  <br/><br/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mongodb/mongodb-plain-wordmark.svg" height="40" alt="MongoDB" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg" height="40" alt="MySQL" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/amazonwebservices/amazonwebservices-original.svg" height="40" alt="AWS" />
</div>

---

## 🚀 Projects & Collaborations

### TechBash Notes App  
• Built with HTML, CSS & JavaScript; migrating to Vite-React with Three.js, GSAP & Glassmorphism for enhanced UI/UX.


#### Key Collaboration  
- **Cloud Minds Team**: With *Nawaz Sayyad* & *Mayuresh Muluk*, secured 3rd prize at the AWS Ideathon for an LLM fine-tuning prototype (SFLLM).

---

## 🎓 Certifications & Achievements
- **Diploma**, VAPM Latur – Completed 2024  
- **Cisco Introduction to Data Science** – Data Analytics & AI/ML fundamentals  
- **INFOSYS-SPRINGBOARD**: Basics of Python  
- **LinkedIn Learning**: Project Management Foundations  
- Multiple hackathon & workshop participations (Innovation Foundation, RAILMIT, DEVTOWN, INNOTECH)

---

## 🔥 My GitHub Stats
<div align="center">
  
<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=prathmbavge&theme=dark&hide_border=false" alt="GitHub Streak Stats" />
</p>

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=prathmbavge&show_icons=true&theme=dark&hide_border=false" alt="GitHub Stats" />
</p>

<p align="center">
  <img src="https://github-profile-trophy.vercel.app/?username=prathmbavge&theme=onedark&margin-w=10&row=1&column=6" alt="GitHub Trophies" />
</p>
</div>

---

_“Striving to build solutions that blend innovation with impact.”_

# simple_linear_regression_advertising.py
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression

# 1️⃣ Load dataset (ensure 'Advertising.csv' is in the same folder)
data = pd.read_csv("Advertising.csv")

# Use TV as predictor and Sales as target
X = data[['TV']]      # feature must be 2D
y = data['Sales']     # target

# 2️⃣ Fit simple linear regression
model = LinearRegression()
model.fit(X, y)

print("Intercept:", model.intercept_)
print("Slope:", model.coef_[0])
print(f"R² score: {model.score(X, y):.3f}")

# 3️⃣ Plot scatter + regression line
plt.figure(figsize=(7,5))
plt.scatter(X, y, color='blue', label='Data Points')
plt.plot(X, model.predict(X), color='red', linewidth=2, label='Regression Line')
plt.xlabel('TV Advertising Budget ($1000s)')
plt.ylabel('Sales (in 1000s units)')
plt.title('Simple Linear Regression: TV vs Sales')
plt.legend()
plt.show()
