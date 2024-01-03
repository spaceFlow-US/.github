# spaceFlow LLC

spaceFlow is a proptech company with a mission to  transform rental income into a passive stream using full rental automation. 

Our platform leverages IoT devices and AI to streamline the entire rental process. In the pre-contract stage, we offer identity verification, secure self tours, background checks, online applications, and eSign capabilities. During the contract, we provide a rent payment system and maintenance ticket system. After the contract, our platform handles room recovery and credit systems, freeing landlords from active involvement and transforming rental income into a truly passive stream.

At spaceFlow, we are committed to revolutionizing the rental industry through cutting-edge technology. Our platform serves as a catalyst for maximizing space utilization and ensuring a seamless rent flow. We transform the way properties are managed, making space utilization more efficient and rent management an effortless experience.

## Problem
Base on Zumper, average room idle time is 42 days.

Because
1. Even professional agent can conduct up to 10 room tours per week, not to mention landlords.
2. Weekdays room tour is 9am - 5pm, but busy tenant are free after 7pm.

## Solution
Self tour

## How large the market?
According to US Census Bureau, there are 24M individual landlord owned rental housing units.

According to Zumper, self tour can shorten 0.3 month room idle time.

Assume each unit is $1000/Mo.

Self tour can save 7.2B per year.

## Potential
- Enables agents to conduct up to 30 tours per day, maximizing the number of visits and significantly enhancing the likelihood of successful deal closures, without requiring physical presence.
- Facilitates remote management for multi-property holders nationwide, enabling efficient and effective property management from any location.

## Pitch Deck
- [Sheet](https://docs.google.com/spreadsheets/d/1BViheaBCrXD0x2fArpVnu0dqRzkXZJQ4UsFLsZ8C3Y8/edit?usp=sharing)
- [Slide](https://docs.google.com/presentation/d/1mOHJSB7zn1kANBHeg-8qv2BKCFXFBA6d_E6fMQoF3kk/edit?usp=sharing)

## Team Intro
[![team intro v2](https://img.youtube.com/vi/mUldCkwMCzc/0.jpg)](https://www.youtube.com/watch?v=mUldCkwMCzc)

## Demo
### Booking
[![booking](https://img.youtube.com/vi/y3k3G9zZv2Q/0.jpg)](https://www.youtube.com/watch?v=y3k3G9zZv2Q)

### Unlock Smart Lock
[![booking](https://img.youtube.com/vi/X2X61lqbVdc/0.jpg)](https://www.youtube.com/watch?v=X2X61lqbVdc)

### Self Tour
[![self tour](https://img.youtube.com/vi/rwv1JMOYAu8/0.jpg)](https://www.youtube.com/watch?v=rwv1JMOYAu8)

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

## Motivation

My name is Sung-Fu Han, and I've been a software engineer and part-time landlord in Taiwan for the past 10 years. I manage properties scattered across Taipei City, New Taipei City, and Kaohsiung. However, the challenges of in-person property tours have led me to embark on an exciting new venture.

Taipei's notorious traffic has proven to be a nightmare, making it a struggle to travel from one rental property to another. Even when I manage to arrive on time, tenants sometimes cancel the room tours for various reasons, leaving me feeling frustrated and inefficient.

To address this issue, I believe that in-person room tours are not only inefficient but also impractical, especially when landlords are not always available at the property. What if they're on vacation and a potential tenant wants a tour? That's when I had a revolutionary idea – self-guided tours! This would allow tenants to explore the property at their convenience without the need for me to be physically present.

However, I understand the safety concerns associated with self-tours, especially in well-decorated properties where the risk of damage or theft is higher. Installing web cameras to monitor the tours seems like a solution, but it introduces extra efforts, and tenants may worry about their privacy even after the cameras are removed.

To overcome these challenges, I'm introducing the "Zero Installation Self Tour." We ensure tour safety only depends on tenant's phone camera. During the tour, we kindly request tenants to grant permissions for their front and rear phone cameras. This enables us to stream the captured footage to an advanced AI-driven malicious event detection system, which aids in identifying any potential instances of missing or damaged objects. Moreover, the stream can also be utilized by tenants to provide evidence of their innocence if need.

But my vision doesn't stop there. I'm driven by a larger dream – to fully automate the entire rental process and turn renting a house into a genuine passive income stream. 

To achieve this, I will automate each part in rental life cycle. I've divided the rental process into three essential parts: before-contract, in-contract, and after-contract. Before-contract services involve recruiting the right tenants through self-tours, identity verification, background checks and eSign. In-contract features include monthly rent payment systems, and maintenance ticket system to address any issues promptly. After-contract includes credit system and room rollback service to ensure the property can rejoin listing automatically.

I firmly believe that automating the entire rental process is feasible, and self tour is last mile. It's surprising that there's no holistic solution available in the market yet. With this conviction, I've decided to take the lead and turn my vision into reality. My mission is to make entire rental process more efficent. Together, we'll make renting a house a true passive income.

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

## Tech Stack
![JavaScript](https://img.shields.io/badge/JavaScript-323330?style=for-the-badge&logo=javascript&logoColor=F7DF1E)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Nodejs](https://img.shields.io/badge/-Nodejs-339933?style=for-the-badge&logo=Node.js&logoColor=ffffff)
![Google Cloud](https://img.shields.io/static/v1?style=for-the-badge&message=Google+Cloud&color=4285F4&logo=Google+Cloud&logoColor=FFFFFF&label=)

## Domain 
[spaceflow.in](https://www.spaceflow.in)

> [spaceflow.io](https://spaceflow.io) is taken by a [real estate company](https://www.linkedin.com/company/spaceflow/?originalSubdomain=cz) in Prague which has the similar mission with us. However, they focus on in-contract management. On the other hand, we focus on entire rental life cycle.


