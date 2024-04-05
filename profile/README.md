# spaceFlow

## Platform
https://tour.getspaceflow.com

## Services
| Activity/Platform       | Tenant                                   | Landlord                                     |
| ----------------------- | ---------------------------------------- | -------------------------------------------- |
| Add new room to Market  |                                          | Web                                          |
| Verification            | Web                                      | Web                                          |
| Book Self Tour          | Mobile/Web                               |                                              |
| Take Self Tour          | Mobile                                   | Web                                          |
| Background Check        |                                          | Web                                          |
| Sign Contract           | Mobile/Web                               | Web                                          |
| Pay Deposit             | Mobile/Web                               |                                              |
| File Mantainance Ticket | Mobile/Web                               |                                              |
| Pay Rent                | Mobile/Web                               |                                              |


## Short Intro

spaceFlow is redefining property management through innovation in proptech. Our mission: to make remote property management a reality.

We understand that high-quality tenants are the backbone of a thriving rental market. At spaceFlow, we enable these tenants to enjoy an express rental experience, deserving of their status. Our platform offers a comprehensive one-time verification process, streamlining their journey from searching to settling into their new home with features like self-guided tours powered by IoT and computer vision, direct video communication with landlords, and swift application processes. This efficiency doesn't just attract tenants; it transforms them into invaluable assets for landlords, acting as reliable, single-unit property managers empowered by spaceFlow's maintenance system.

With just a few clicks to list a property and a monthly platform fee, landlord gain access to a pool of qualified tenants. Our automation platform will guide qualified tenants to handle the rest. Landlords can live anywhere.

Join us at spaceFlow, where we leverage cutting-edge technology to streamline the rental process, build strong landlord-tenant relationships, and pave the way for the future of remote property management. Transforming the rental industry, one property at a time. Invest in homes like stocks, earn dividends effortlessly.

## Target Audience
![image](https://github.com/spaceFlow-US/.github/assets/20626329/d977294b-8132-4a19-bce5-bbdb617f5576)



## Problem
According to data from Zumper, the average room in the rental market remains idle for an extended period of 42 days. This inefficiency primarily stems from a mismatch between tenant availability and landlord or agent schedules. Professional agents, handling up to 10 room tours per week, typically operate during standard business hours (9 AM - 5 PM), which conflicts with the schedules of busy tenants who are often only available after 7 PM. Additionally, the concept of self-tours, though convenient, is not widely embraced due to prevailing trust issues.

## Solution
Our product aims to revolutionize the rental market by making self-tours a popular and trusted option.

How We Achieve This:

We plan to build trust between landlords and tenants in the pre-contract stage through innovative technology. This includes:

- Supervised Computer Vision for Landlords: To provide real-time oversight during self-tours, enhancing security and trust.
- Rigorous Tenant ID Checks: To ensure the authenticity and reliability of potential tenants.
- Mandatory Tenant Credit Card Registration: To secure financial accountability and provide assurance to the landlord.

By implementing these technological solutions, we bridge the gap between landlords and tenants, significantly reducing room idle time and streamlining the rental process.


## How large the market?
According to US Census Bureau, there are 24M individual landlord owned rental housing units.

According to Zumper, self tour can shorten 0.3 month room idle time.

Assume each unit is $1000/Mo.

Self tour can save 7.2B per year.

## Potential
- Enables agents to conduct up to 30 tours per week, maximizing the number of visits and significantly enhancing the likelihood of successful deal closures, without requiring physical presence.
- Facilitates remote management for multi-property holders nationwide, enabling efficient and effective property management from any location.

## Pitch Deck
- [Sheet](https://docs.google.com/spreadsheets/d/1BViheaBCrXD0x2fArpVnu0dqRzkXZJQ4UsFLsZ8C3Y8/edit?usp=sharing)
- [Slide](https://docs.google.com/presentation/d/1mOHJSB7zn1kANBHeg-8qv2BKCFXFBA6d_E6fMQoF3kk/edit?usp=sharing)

## Team Intro
[![team intro v2](https://img.youtube.com/vi/mUldCkwMCzc/0.jpg)](https://www.youtube.com/watch?v=mUldCkwMCzc)

| Name                                                            | Role  | Background                                   |
| --------------------------------------------------------------- | ----- | -------------------------------------------- |
| [Sung-Fu Han](https://www.linkedin.com/in/sungfuhan/)           |  CEO  | 10y Landlord/SRE/ML Reseacher                |
| [Yi-Kai Liao](https://www.linkedin.com/in/yi-kailiao/)          |  CTO  | 3y Tenant/Leetcode 1300 solved               |
| [Nelly Shih](https://www.linkedin.com/in/nellyshih/)            |  UX   | Yahoo UX/Struggle on real estate transparency|
| [Takuma Takezawa](https://www.linkedin.com/in/takuma-takezawa/) |  SDE  | Airbnb Host                                  |


## User Flow

### Tenant
**[Book tour](https://youtu.be/UOzoPsOO0no)**: Login -> product page -> (phone/ID/Credit card verification) ->Book tour -> got approved 

### Landlord
**Add room**: Login -> Property Page -> upload room info -> grant smart lock permission -> room added

**[Approve Tour](https://youtu.be/pFf5CD-o4cg)**: Login -> schedule page -> approve or deny inquired tour

### Tenant & Landlord
**[Cloud tour](https://youtu.be/lp7MuM7jdvM)**: schedule page -> cloud tour -> unlock -> tour completed -> video upload

## Progress

|Rental Lifecycle | Before-contract | In-contract | After-contract | 
|-|-|-|-|
|Porjects| Frontier Map Search :fire: <br>  ID Check <br> Self Tour :fire: <br> Background Check <br> eSign | Pay Rent System <br> Maintainence Ticket System <br> Tenant Web App <br> Landlord Web App :fire: | Credit System |

![image](https://github.com/spaceFlow-US/.github/assets/20626329/1e237faf-43db-4eba-b639-1021af38717d)


## Culture
- [Fight on](https://www.youtube.com/watch?v=RQ7oArZrQ1s&t=73s&ab_channel=CaliforniasGold)
- Perfection
- Curiosity
- Passion

## Design Principles
- SOLID
- DRY (Don't Repeat Yourself)
- KISS (Keep It Simple, Stupid)
- YAGNI (You Aren't Gonna Need It)
- Refactor Regularly

## Motivation

My name is Sung-Fu Han, and I've been a software engineer and part-time landlord in Taiwan for the past 10 years. I manage properties scattered across Taipei City, New Taipei City, and Kaohsiung. However, the challenges of in-person property tours have led me to embark on an exciting new venture.

Taipei's notorious traffic has proven to be a nightmare, making it a struggle to travel from one rental property to another. Even when I manage to arrive on time, tenants sometimes cancel the room tours for various reasons, leaving me feeling frustrated and inefficient.

To address this issue, I believe that in-person room tours are not only inefficient but also impractical, especially when landlords are not always available at the property. What if they're on vacation and a potential tenant wants a tour? That's when I had a revolutionary idea – self-guided tours! This would allow tenants to explore the property at their convenience without the need for me to be physically present.

However, I understand the safety concerns associated with self-tours, especially in well-decorated properties where the risk of damage or theft is higher. Installing web cameras to monitor the tours seems like a solution, but it introduces extra efforts, and tenants may worry about their privacy even after the cameras are removed.

To overcome these challenges, I'm introducing the "Zero Installation Self Tour." We ensure tour safety only depends on tenant's phone camera. During the tour, we kindly request tenants to grant permissions for their front and rear phone cameras. This enables us to stream the captured footage to an advanced AI-driven malicious event detection system, which aids in identifying any potential instances of missing or damaged objects. Moreover, the stream can also be utilized by tenants to provide evidence of their innocence if need.

But my vision doesn't stop there. I'm driven by a larger dream – to fully automate the entire rental process and turn renting a house into a genuine passive income stream. 

To achieve this, I will automate each part in rental life cycle. I've divided the rental process into three essential parts: before-contract, in-contract, and after-contract. Before-contract services involve recruiting the right tenants through self-tours, identity verification, background checks and eSign. In-contract features include monthly rent payment systems, and maintenance ticket system to address any issues promptly. After-contract includes credit system and room rollback service to ensure the property can rejoin listing automatically.

I firmly believe that automating the entire rental process is feasible, and self tour is last mile. It's surprising that there's no holistic solution available in the market yet. With this conviction, I've decided to take the lead and turn my vision into reality. My mission is to make entire rental process more efficent. Together, we'll make renting a house a true passive income.

I'm thrilled to show that despite not being typical young, university-dropout founder, I've taken the traditional route - completing my education and gaining years of work experience. Now, I'm ready to chase my dream and start my own company. This dream is a glowing ember within me, and with persistence, it will ignite into a blazing success!

## Q&A
**Q1: Why do you ask tenants to use their phones for a video tour instead of installing a camera in the room?**

A: There are several reasons for this approach. Firstly, having a camera in the room can make tenants feel insecure, a feeling that might persist during their stay. Using their phones, tenants can choose specific areas to focus on, and later compare these with other videos. This method also avoids the need for landlords to install additional equipment. Most importantly, it helps tenants feel safer and more in control of their privacy.

**Q2: Why prefer physical tours over virtual tours?**

A: Virtual tours like Matterport offer a great preview, but they fall short in capturing the essence of a property. Tenants often need to experience aspects like the neighborhood vibe, natural light, and feel of the space in person before making a commitment. That's why, despite the convenience of virtual tours, physical self-tours remain crucial for final decision-making.

**Q3: What is the different between spaceFlow and other property management software such as appfolio, doorloops, turbotenant and hemlane?**

A: spaceFlow distinguishes itself in the property management sector by prioritizing the rental experience of highly qualified tenants. While traditional software solutions cater to landlords and property managers, 50% property owners still choose self-management, indicating a gap that existing platforms do not address. spaceFlow believe qualify tenants deserve express rental experience. Qaulified tenants are who meet strict qualifications, including ID verification, credit card linkage, a credit score above 700, a clean criminal record, verified income, and no history of eviction. By focusing on these tenants, who are effectively single-unit property managers, spaceFlow enhances their autonomy, strengthening trust with landlords and facilitating remote property management. This shift to tenant-centered features promises to attract landlords by providing them the assurance of a responsible occupant and a hands-off management approach.

**Q9: How to make self tour everywhere?**

GPT: Making self-guided property tours available everywhere involves a combination of technology, security, and logistical planning. Here's a general strategy to achieve this:

1. Develop a Reliable Technology Platform: Create or utilize an existing platform that allows potential tenants to schedule and access properties without needing a physical agent present. This platform should handle scheduling, identity verification, and secure access.

2. Implement Secure Access Systems: Install smart locks or lockbox systems that can be controlled remotely. These systems should allow access only to verified individuals and at the scheduled times.

3. Identity Verification: Ensure that all users of the self-tour service undergo a robust identity verification process. This could include submitting government-issued ID and a current photograph, and possibly credit card information for security purposes.

4. Real-time Monitoring: Use technology like computer vision or real-time surveillance to monitor tours. This ensures safety for the property and can provide landlords with peace of mind.

5. Feedback and Reporting Mechanisms: After the tour, have an automated system to collect feedback or reports from the potential tenant. This can help in improving the experience and addressing any issues immediately.

6. Marketing and Partnerships: Collaborate with property listing sites, real estate agents, and property management companies to offer self-tour options as a part of their services.

7. Legal Compliance and Insurance: Ensure all activities comply with local real estate laws and regulations. Also, consider insurance to cover any liabilities that might arise from self-tours.

8. Customer Support: Provide excellent customer support to handle any issues, questions, or emergencies during the self-tour.

9. Continuous Improvement: Collect data and feedback to continuously improve the self-tour experience, security, and technology.

10. Scalability Plan: Have a clear plan for scaling the service, including expanding to new locations, managing increasing numbers of tours, and ensuring consistent quality and security as you grow.

Implementing self-tours everywhere is a complex task that requires careful consideration of security, technology, and user experience, but with the right approach, it can significantly enhance the property rental process.

## Tech Stack

| Frontend      | API        | Backend        | DB              | Cloud          |
| ------------- | ---------- | -------------- | --------------- | -------------- |
| ![React Native](https://img.shields.io/static/v1?style=for-the-badge&message=React+Native&color=61DAFB&logo=React&logoColor=FFFFFF&label=) ![JavaScript](https://img.shields.io/badge/JavaScript-323330?style=for-the-badge&logo=javascript&logoColor=F7DF1E) ![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB) | ![Stripe](https://img.shields.io/static/v1?style=for-the-badge&message=Stripe&color=5433FF&logo=Stripe&logoColor=FFFFFF&label=) ![Seam API](https://img.shields.io/static/v1?style=for-the-badge&message=Seam+API&color=00BFFF&logo=Seam&logoColor=FFFFFF&label=) | ![Nodejs](https://img.shields.io/badge/-Nodejs-339933?style=for-the-badge&logo=Node.js&logoColor=ffffff) ![Python](https://img.shields.io/static/v1?style=for-the-badge&message=Python&color=3776AB&logo=Python&logoColor=FFFFFF&label=) | ![Firebase](https://img.shields.io/static/v1?style=for-the-badge&message=Firebase&color=FFCA28&logo=Firebase&logoColor=FFFFFF&label=) | ![Google Cloud](https://img.shields.io/static/v1?style=for-the-badge&message=Google+Cloud&color=4285F4&logo=Google+Cloud&logoColor=FFFFFF&label=) |




<!-- 

## Domain 
[spaceflow.in](https://www.spaceflow.in)

> [spaceflow.io](https://spaceflow.io) is taken by a [real estate company](https://www.linkedin.com/company/spaceflow/?originalSubdomain=cz) in Prague which has the similar mission with us. However, they focus on in-contract management. On the other hand, we focus on entire rental life cycle.


## Design Story - Cloud Tour
Let take Airbnb website as a role model.

Think you are a tenant and is searching for a room to rent at least 3 month or longer.

### A. you searching for a location and see many rooms

![Image](https://user-images.githubusercontent.com/20626329/249678185-feea43b2-4ac8-4a2b-a5a9-5532cbdfa752.png)

### B. you pickup a place that close to your company and detail page shows

![Image](https://user-images.githubusercontent.com/20626329/249679522-24202d46-d812-46ad-a3d2-8534a25693eb.png)

### C. you want to have a room tour so you click "book a room tour" button

> Our works start from this button

### D. User Experience Flow
The purpose of this document is to outline the design for building an entire tour experience starting from a button. The tour experience includes creating a unique room tour transaction, embedding the tour link in Google Calendar, confirming the tour, granting necessary permissions, matching GPS location, unlocking the smart lock, conducting the tour, detecting malicious events through AI, and completing the tour with a credit increase.

#### 1. Creating a Unique Room Tour Transaction
- When a tenant selects a valid time provided by the landlord in Calendly, a unique room tour transaction should be created in the Firebase Realtime Database.
- The transaction should include relevant details such as the tenant, landlord, tour time, and room information.
- The unique room tour link should be embedded in the tenant and landlord's Google Calendar, ensuring easy access for both parties.

#### 2. Confirmation and Permission
- At the scheduled tour time, the tenant should physically arrive at the location.
Using their phone, the tenant opens the unique tour link in the web app, which leads to the confirmation page.
- The web app requests permission to access the GPS, front camera, and rear camera of the tenant's device.
- Granting these permissions is necessary for security purposes and to proceed with the room tour.

#### 3. GPS Location Match and Smart Lock Unlock
- Once the landlord is online, the web app checks if the tenant's GPS location matches the location recorded in the transaction.
- If the GPS location matches, the smart lock associated with the room will be unlocked, signaling the start of the room tour.

#### 4. Room Tour Process
- During the tour, the tenant can ask questions to the landlord or an online agent for assistance.
- The video stream from the tenant's device will be sent to an AI server for detecting any malicious events, such as stealing or breaking something.
- The AI server analyzes the video stream in real-time and alerts appropriate parties if it detects any suspicious activities.

#### 5. Tour Completion and Credit Increase
- When the room tour is completed, the smart lock will automatically lock the room.
- If there are no security issues detected during the tour, the tenant's credit will increase by a certain amount as a reward for completing the tour.

Note: This design document provides a high-level overview of the room tour experience. Implementation details, technical specifications, and security measures should be further defined during the development process. 

-->


