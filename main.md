<style>
  /* General font and colors */
  body {
    font-family: 'DM Sans', Arial, sans-serif;
    color: #a72121;
    line-height: 1.6;
  }

  /* Title page styling */
  .title-page {
    text-align: center;
    margin-top: 80px;
    margin-bottom: 120px;
  }
  .title-page h1 {
    font-size: 3.5em;
    margin-bottom: 0.2em;
  }
  .title-page h2 {
    font-weight: 400;
    margin-bottom: 2em;
    color: #555;
    font-size: 1.8em;
  }

  /* Team table: 2 columns, right-align left col, left-align right col, no header, no borders */
  .team-table {
    margin: 0 auto 3em auto;
    width: 600px;
    border-collapse: collapse;
  }
  .team-table tr {
    border: none;
  }
  .team-table td {
    padding: 8px 20px;
    vertical-align: middle;
  }
  .team-table td:first-child {
    text-align: right;
    font-weight: 600;
    padding-right: 4px;
    width: 50%;
  }
  .team-table td:last-child {
    text-align: left;
    width: 50%;
  }

  /* Date styling */
  .date-text {
    font-style: italic;
    font-size: 1em;
    color: #777;
  }

  /* Section headings */
  h1, h2, h3 {
    font-family: 'DM Sans', Arial, sans-serif;
    font-weight: 700;
    color: #a72121;
  }

  /* TOC page */
  .toc-page {
    page-break-before: always;
    max-width: 600px;
    margin: 60px auto 0 auto;
    text-align: center;
  }
  .toc-page h2 {
    margin-bottom: 0.3em;
    font-size: 2.5em;
  }
  .toc-intro {
    font-size: 1.1em;
    color: #555;
    margin-bottom: 2em;
    font-weight: 500;
  }
  .toc-list {
    text-align: left;
    font-size: 1.1em;
    max-width: 400px;
    margin: 0 auto;
    line-height: 1.7;
  }
  .toc-list li {
    margin-bottom: 0.7em;
  }

  /* Page break for print/PDF */
  .page-break {
    page-break-before: always;
  }
</style>

<div class="title-page">
  <h1>UniShare</h1>
  <h2>University Trading App</h2>
  <strong>TEAM TLPs</strong>

  <table class="team-table">
    <tbody>
      <tr><td>Justine Bautista</td><td>Project Manager / UI-UX Designer</td></tr>
      <tr><td>Mark Jason Fulguerinas</td><td>Frontend Developer</td></tr>
      <tr><td>Charles Ezra Ilarde</td><td>Backend Developer</td></tr>
      <tr><td>Regie San Juan</td><td>Quality Engineer / Frontend Developer</td></tr>
    </tbody>
  </table>

  <p class="date-text"><em>Date: <!-- Insert today's date --></em></p>
</div>

<div class="toc-page page-break">
  <h2>Table of Contents</h2>
  <p class="toc-intro">Explore the sections of this document below:</p>
  <ul class="toc-list">
    <li><a href="#abstract">Abstract</a></li>
    <li><a href="#introduction">Introduction</a></li>
    <li><a href="#system-architecture">System Architecture</a></li>
    <li><a href="#features">Features</a></li>
    <li><a href="#technology-stack">Technology Stack</a></li>
    <li><a href="#karma-credit-system">Karma Credit System</a></li>
    <li><a href="#impact-and-sustainability">Impact and Sustainability</a></li>
    <li><a href="#conclusion">Conclusion</a></li>
  </ul>
</div>

<div class="page-break"></div>

# Table of Contents

- [Abstract](#abstract)  
- [Introduction](#introduction)  
- [System Architecture](#system-architecture)  
- [Features](#features)  
- [Technology Stack](#technology-stack)  
- [Karma Credit System](#karma-credit-system)  
- [Impact and Sustainability](#impact-and-sustainability)  
- [Conclusion](#conclusion)  

---

## Abstract

UniShare is a dedicated university trading platform designed to streamline the buying, selling, and borrowing of goods among students within campus. Unlike currency trading, UniShare focuses on physical items, regulated by a karma credit system to encourage trust and accountability. Leveraging modern web technologies and AWS cloud services, UniShare provides a secure, efficient, and user-friendly marketplace that fosters sustainable campus commerce.

---

## Introduction

Students frequently use social media pages like Facebook groups to buy, sell, or borrow items, but these platforms lack regulation and accountability, leading to issues like lost or damaged borrowed items. UniShare aims to solve this by offering a dedicated university trading app where students can post items for sale, trade, or borrow with agreed time limits. The platform regulates user behavior through a karma credit system that deducts points for damage or late returns, influencing users' trading and borrowing limits. This promotes responsibility and trust within the community.

---

## System Architecture

<figure>
  <div style="border:1px solid #ddd; padding: 2em; background: #f5faff; color: #a72121; font-weight: bold; max-width: 800px; margin: auto;">
    [Placeholder for AWS System Architecture Diagram]
  </div>
  <figcaption>Figure 1: UniShare AWS Architecture Diagram</figcaption>
</figure>

UniShare uses a serverless backend hosted on AWS Lambda to handle business logic, integrated with API Gateway for RESTful APIs. PostgreSQL serves as the main database for persistent data, hosted on Amazon RDS or an external managed PostgreSQL service. React is used for the frontend application, communicating via secured API endpoints. Additional AWS services ensure security, scalability, and monitoring.

---

## Features

| No. | Feature Description                                                  |
|-----|--------------------------------------------------------------------|
| 1   | User authentication with university verification (AWS Cognito suggested) |
| 2   | Item listing with photos, descriptions, and pricing                 |
| 3   | Search and filtering by category, price, and location               |
| 4   | In-app chat for negotiations and communication                      |
| 5   | Karma credit system regulating trading and borrowing limits         |
| 6   | Reporting and moderation for community safety and security          |

---

## Technology Stack

| Category          | Technology / Tool                | Description                           |
|-------------------|---------------------------------|-------------------------------------|
| Frontend          | React.js                       | Responsive and dynamic UI framework  |
| Backend           | Laravel PHP                    | PHP framework serving API endpoints  |
| Database          | PostgreSQL                    | Reliable, relational data storage    |
| AWS Services      | AWS Lambda                    | Serverless compute functions         |
|                   | Amazon API Gateway            | Secure API management                |
|                   | AWS Cognito                   | User authentication and university verification |
|                   | Amazon RDS / Neon Serverless Postgres | Managed PostgreSQL database services |
|                   | Amazon S3                     | Secure storage for user-uploaded photos |
|                   | AWS CloudWatch                | Monitoring and logging service       |
|                   | AWS WAF and AWS Shield        | Security and DDoS protection          |
| Development Tools | GitHub                       | Version control and collaboration    |
|                   | Figma                        | UI/UX design prototypes              |
|                   | LaTeX                        | Documentation writing                |

---

## Karma Credit System

UniShare incorporates a karma-based credit system to encourage responsible behavior in trading and borrowing items.

### How it Works

- Each user starts with a baseline karma score (e.g., 100 points).  
- Borrowing or trading limits (e.g., maximum number of items, borrowing duration) depend on the user's current karma.  
- Karma points are deducted for:  
  - Damaged items upon return.  
  - Late returns beyond agreed borrowing period.  
  - Failure to return borrowed items.  
  - Negative reports verified by moderators.  
- Karma points are restored gradually through positive transactions and community feedback.

### Impact of Karma Score

- High karma users enjoy higher borrowing limits and longer borrowing periods.  
- Low karma users face restrictions or temporary bans from borrowing/trading.  
- The system promotes trustworthiness and accountability in the community.

### Example

If a user forgets to return an item on time, 10 karma points are deducted. If karma drops below 50, the user can only borrow one item at a time and for a shorter duration. Users can recover karma by completing successful trades or receiving positive reviews.

---

## Impact and Sustainability

UniShare fosters a trusted, peer-to-peer marketplace exclusively for the university community, reducing reliance on external social media groups that lack accountability. This encourages sustainable consumption by promoting reuse, sharing, and borrowing, reducing waste and unnecessary purchases. The karma credit system builds a culture of responsibility and trust, leading to long-term community benefits.

---

## Conclusion

UniShare offers a secure, well-regulated platform tailored for university students to trade, sell, or borrow items with confidence. By leveraging AWS cloud services and a thoughtful karma credit system, it ensures accountability, scalability, and sustainability. Future improvements include adding more advanced AI-based fraud detection, expanding to other campuses, and enhancing user engagement features.

