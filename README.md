# Image-Based Graphical Password Authentication System

## Abstract

Image-based graphical password systems leverage human visual and cognitive capabilities to create memorable and secure authentication mechanisms. This system leverages images and user-defined graphical passwords to provide a more secure and user-friendly authentication mechanism. Users can set up their graphical passwords by selecting specific points on an image, and these points will be used for authentication during login. The system stores the images and corresponding graphical password data. The research aims to demonstrate the feasibility and effectiveness of graphical password authentication using Flask and assess its security and usability.

## Table of Contents

- [Introduction](#introduction)
- [Literature Survey](#literature-survey)
- [Proposed Method](#proposed-method)
  - [Architecture Overview](#architecture-overview)
  - [Image Upload](#image-upload)
  - [Image-Coordinate-Based Authentication](#image-coordinate-based-authentication)
  - [Security Measures](#security-measures)
  - [User Experience Enhancement](#user-experience-enhancement)
- [Conclusion](#conclusion)

## Introduction

In today's digital landscape, the security of user accounts and data is of paramount importance. To address these concerns, this paper presents a secure image upload and authentication system, leveraging the Flask framework. This authentication approach centers on the utilization of image coordinates, a departure from conventional text-based passwords. By employing this method, the system seeks to bolster security measures while simultaneously enhancing the user experience. The system not only allows users to securely upload images but also introduces an innovative authentication approach that utilizes image coordinates. This method enhances security while maintaining a user-friendly experience, reducing the reliance on text-based passwords. Traditional password-based authentication methods are susceptible to various attacks, including brute force and phishing attacks.

## Literature Survey

[Include your literature survey content here.]

## Proposed Method

### Architecture Overview

The architecture of the proposed system consists of several interconnected components, each serving a specific role in achieving secure image upload and authentication. These components include:

- **Flask Application:** The core application built using Flask, is responsible for handling user interactions, image uploads, and authentication.
- **SQLAlchemy and Database:** The PostgreSQL database managed by SQLAlchemy is used to store user data, uploaded images, and authentication information.
- **Image Upload Module:** Responsible for allowing users to upload images, which are stored as binary data in the database.
- **Authentication Module:** Implements the image-coordinate-based authentication mechanism, comparing user-entered coordinates with stored image patterns.
- **User Information Module:** Manages user information such as email and authentication details.

### Image Upload

The system enables users to securely upload images through the Flask web interface. The uploaded image is associated with the user's account and stored in the PostgreSQL database as binary data. The relevant metadata, including the image's name, MIME type, and user details, are also stored for efficient retrieval.

### Image-Coordinate-Based Authentication

The core innovation of the system lies in its authentication method, which leverages image coordinates for user verification. The process involves the following steps:

1. **Pattern Creation during Registration:** Users select specific coordinates from their uploaded images, creating a unique pattern for authentication. These coordinates are stored in the database along with the user's email and other relevant information.

2. **Authentication during Login:** During login, users are prompted to input image coordinates based on their predefined pattern.

3. The entered coordinates are compared with the stored pattern for a match.

4. **Coordinate Comparison with Tolerance:** The system compares each entered coordinate with the stored coordinates, considering a predefined tolerance range. If the entered coordinates closely match the stored pattern within the tolerance range, authentication is successful.

### Security Measures

To enhance security, the system employs the following measures:

- **Image Data Storage:** Images are stored as binary data, reducing the risk of unauthorized access.
- **Coordinate Tolerance:** The tolerance range minimizes the impact of small variations during authentication, ensuring usability without compromising security.
- **User-Specific Authentication:** The image-coordinate pattern is unique to each user, making it challenging for attackers to replicate.

### User Experience Enhancement

The proposed system aims to maintain a positive user experience while improving security. The image-based authentication method is intuitive, reducing the need for users to remember complex passwords. The familiarity of images and coordinates enhances user comfort and ease of use.

## Conclusion

The research presents a Flask-based secure image upload and authentication system, addressing vulnerabilities of traditional password-based methods. Introducing image-coordinate-based authentication enhances security while maintaining usability. Images are uploaded securely, associating them with user accounts. The evaluation shows this approach offers robust protection and positive user experiences. Future enhancements could include multi-factor authentication, biometric integration, and advanced image analysis, ensuring continued resilience against evolving cyber threats. This system's adaptability and innovation have the potential to reshape online security, contributing to a more secure and user-centric digital landscape.

[Include information on how to set up and run the system, licensing details, and any contact information for support or collaboration.]

