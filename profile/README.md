# spaceFlow LLC

spaceFlow is a technology-driven company with a clear mission to optimize space utilization and facilitate a seamless rental experience.

Our advanced platform offers a comprehensive solution for both landlords, including property agencies, and tenants, automating daily rent management tasks through the utilization of IoT devices such as smart locks, smart meters, and AI cameras. By addressing pain points experienced by both parties, we enhance transparency and foster a more efficient exchange of property information.

One prevalent challenge for landlords arises when tenants express interest in viewing a room in person, necessitating the physical presence of an agent and carrying the risk of potential no-shows. Our groundbreaking solution, the cloud room tour, revolutionizes this process. Landlords or agents can now remain online, awaiting tenants and virtually accompanying them during the room tour. Tenants experience a true-to-life room tour and gain access to the property independently, accompanied by online agents. The entire process is fortified by a secure live camera stream sourced from the tenant's phone, eliminating the need for additional installations, while our sophisticated malicious event detection ensures a safe environment.

Furthermore, our platform seamlessly integrates various rent-related operations, including rent payments, repair requests, contract signing, tenant/landlord credit checks, room advertising, and even legal consulting. By consolidating these essential functions into a single platform, we empower landlords and tenants alike with a centralized hub that streamlines the rental process, saving time and increasing convenience.

At spaceFlow, we are committed to revolutionizing the rental industry through cutting-edge technology and outstanding customer service. Our platform serves as a catalyst for maximizing space utilization and ensuring a seamless rent flow. Join us as we transform the way properties are managed, making space utilization more efficient and rent management an effortless experience.

## Progress

|Rental Lifecycle | Before-contract | In-contract | After-contract | 
|-|-|-|-|
|Porjects| Cloud Tour (ongoing)<br> eSign| Maintainence Ticket System <br> Pay Rent System <br> Landlord Dashborard (ongoing) | Credit System|

## Business Model
- Monthly subscription or on-demand fee
- Smart lock hardware

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

