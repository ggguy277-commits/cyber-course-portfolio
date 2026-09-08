# Cloud Concepts Reflection

## Cloud
- Imagine your photos stored in album and your documents you store are in your closet. Also imagine if there is a system that stores all your papers and photos in online storage or digital space. Well maybe your documents are on computer, but what you going to do if your computer will be hacked or simply not going to work properely and your all files will be gone? This is the reason why cloud exists. You can post your photos, for example, on Instagram and they will be saved there and if you delete your photos not on purpose from your phone, you will be able to save them again from your Instagram profile. This was example of cloud.

## Traditional → Cloud → Containers
- In the begining data stored on physical server, but through the time the amount of data was growing more and more. So the physical storages needed to be more and more, it was expensive and costed a lot of time to install a new server. So they came up with hypervisors which made it possible to split a single device into several parts. This reduced expenditure on physical storage media. But it was not enough. Now they figured out the access to these several parts can be online in the Internet and now you are able to just rent some space in online storage. But still it was a problem in operation system that launched on each several part, it costed resources and time. So they figured out that the several parts can use the same one operation system that the host has. It solved operating system vverhead and environment inconsistency.

## Deployment vs Service models
- They are often confused because deployment models describe where computing resources run, while service models describe what level of control you are given. 
- Deployment models answer the question: Where is the infrastructure running, and who shares it? They define ownership, physical location, and access limits. Public Cloud means infrastructure owned by a third-party provider and shared across multiple customers over the internet. Private Cloud is dedicated exclusively to a single organization. On-Premises means traditional hardware owned and housed in your own building. Hybrid Cloud combines on-premises or private resources with a public cloud, while Multi-Cloud uses services from several distinct public cloud providers.
- Service models answer the question: How much of the technology stack do you manage versus rent? They define where your management responsibilities end and the provider's begin. Infrastructure as a Service (IaaS) provides raw building blocks like virtual servers and storage, leaving operating systems and applications to you. Platform as a Service (PaaS) provides a complete deployment environment where the provider manages the OS and server maintenance while you focus strictly on code. Software as a Service (SaaS) gives you a finished, web-accessible application where the provider manages everything behind the scenes.
- For example Google Docs is a service that is both Public Cloud and SaaS. It is Public Cloud because it runs on Google's massive, shared global infrastructure accessible over the internet rather than on a server sitting in your home or company office. It is SaaS because it is a complete end-user application: you don't manage any servers, operating systems, or storage hardware—you simply open your browser, log in, and start writing.

## The Shared Responsibility Model 
- The Shared Responsibility Model is a framework that defines which security tasks belong to the cloud provider and which remain with the customer. The vendor is responsible for the security of the cloud like the physical data centers, host hardware, and global infrastructure, while you remain responsible for security in the cloud: your data, user access, and configuration settings.

## Why organisations still hesitate
- There are laws (GDPR or national law) which require, for example, banks or hospitals to store their data in a specific geographical location, and so switching to cloud storage is impossible. Also there are situations when servers need to run continuously, seven days a week, and in such cases it turns out that maintaining physical servers is cheaper than paying for cloud server hosting.

## Cloud in an entry-level tech role
- A marketing team member submits an urgent ticket stating that a public download link for a company whitepaper is returning a "403 Forbidden" error message instead of serving the PDF file.
- An IT-support recieves massage that user from Helsinki logged into Microsoft 365 and then 15 minutes later the same user loggining from Sao Paulo Brazils IP address.

## Personal takeaway
- Now I know the history of cloud storage and the reasons behind it. I know who is on the other side of the cloud servers when I publish my data online. Now I also know various methods of data storage.
