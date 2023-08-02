# spaceFlow LLC

spaceFlow is a technology-driven company with a clear mission to optimize space utilization and facilitate a seamless rental experience.

Our advanced platform offers a comprehensive solution for both landlords, including property agencies, and tenants, automating daily rent management tasks through the utilization of IoT devices such as smart locks, smart meters, and AI cameras. By addressing pain points experienced by both parties, we enhance transparency and foster a more efficient exchange of property information.

One prevalent challenge for landlords arises when tenants express interest in viewing a room in person, necessitating the physical presence of an agent and carrying the risk of potential no-shows. Our groundbreaking solution, the cloud room tour, revolutionizes this process. Landlords or agents can now remain online, awaiting tenants and virtually accompanying them during the room tour. Tenants experience a true-to-life room tour and gain access to the property independently, accompanied by online agents. The entire process is fortified by a secure live camera stream sourced from the tenant's phone, eliminating the need for additional installations, while our sophisticated malicious event detection ensures a safe environment.

Furthermore, our platform seamlessly integrates various rent-related operations, including rent payments, repair requests, contract signing, tenant/landlord credit checks, room advertising, and even legal consulting. By consolidating these essential functions into a single platform, we empower landlords and tenants alike with a centralized hub that streamlines the rental process, saving time and increasing convenience.

At spaceFlow, we are committed to revolutionizing the rental industry through cutting-edge technology and outstanding customer service. Our platform serves as a catalyst for maximizing space utilization and ensuring a seamless rent flow. Join us as we transform the way properties are managed, making space utilization more efficient and rent management an effortless experience.

## Progress

|Rental Lifecycle | Before-contract | In-contract | After-contract | 
|-|-|-|-|
|Porjects|  Cloud Tour :fire: <br> eSign| Maintainence Ticket System <br> Pay Rent System <br> Landlord Dashborard :fire:| Credit System|

## Customer
- Property Management Company
- Multi-Property Holders

## Business Model
- Monthly subscription or on-demand fee
- Ultra power saving smart lock

## Potential
- Enables agents to conduct up to 30 tours per day, maximizing the number of visits and significantly enhancing the likelihood of successful deal closures, without requiring physical presence.
- Facilitates remote management for multi-property holders nationwide, enabling efficient and effective property management from any location.

## Motivation

My name is Sung-Fu Han, and I've been a software engineer and part-time landlord in Taiwan for the past 10 years. I manage properties scattered across Taipei City, New Taipei City, and Kaohsiung. However, the challenges of in-person property tours have led me to embark on an exciting new venture.

Taipei's notorious traffic has proven to be a nightmare, making it a struggle to travel from one rental property to another. Even when I manage to arrive on time, tenants sometimes cancel the room tours for various reasons, leaving me feeling frustrated and inefficient.

To address this issue, I believe that in-person room tours are not only inefficient but also impractical, especially when landlords are not always available at the property. What if they're on vacation and a potential tenant wants a tour? That's when I had a revolutionary idea – self-guided tours! This would allow tenants to explore the property at their convenience without the need for me to be physically present.

However, I understand the safety concerns associated with self-tours, especially in well-decorated properties where the risk of damage or theft is higher. Installing web cameras to monitor the tours seems like a solution, but it introduces extra efforts, and tenants may worry about their privacy even after the cameras are removed.

To overcome these challenges, I'm introducing the "Zero Installation Self Tour." This innovative solution is perfect for landlords with decorated properties or those who require video tours. With this system, tenants can experience the property virtually without any physical installations or privacy concerns.

But my vision doesn't stop there. I'm driven by a larger dream – to fully automate the entire rental process and turn renting a house into a genuine passive income stream. As a dedicated software engineer, my goal is to focus on my profession and achieve career growth while the rental process runs seamlessly in the background.

To achieve this, I've divided the rental process into three essential parts: before-contract, in-contract, and after-contract. Before-contract services involve recruiting the right tenants through self-tours, background checks, financial capability assessments, and online communication between landlords and tenants.

In-contract features include convenient contract eSign, secure deposit and monthly rent payment systems, and a daily maintenance ticket system to address any issues promptly.

My plans for the after-contract phase includes move-out photo checks and cleaning service requests to ensure the property is ready for the next tenant. For the final part, third-party cleaning services can help restore the property to its initial state, allowing it to back to next rental life cycle quickly.

I firmly believe that automating the entire rental process is feasible, and it's surprising that there's no mature solution available in the market yet. With this conviction, I've decided to take the lead and turn my vision into reality.

My mission is to empower landlords and revolutionize the rental industry. Together, we'll make renting a house a true passive income opportunity, free from the burdens of traditional property management.

## Design Story
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
[spaceflow.in](https://cloudtour.spaceflow.in)

> [spaceflow.io](https://spaceflow.io) is taken by a real [estate company](https://www.linkedin.com/company/spaceflow/?originalSubdomain=cz) in Prague which has the similar mission with us. However, they focus on after contract management. On the other hand, we focus on before contract. Futhermore, our dev tean members comes from world class CS program around the valley. Therefore, the market is ours.




## Logo
![logo](https://github.com/wallinslax/spaceFlow/assets/20626329/9282f845-7f35-4715-b55f-188f8ecfd576)

