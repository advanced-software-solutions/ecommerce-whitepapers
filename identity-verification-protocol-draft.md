# Identity Verification Protocol - IVP 

**Status:** Draft
**Version:** 1.0
**Last Updated:** 2026-02-21
**Author:** Amr Swalha - Advanced Software Solutions

---

## Executive Summary

This whitepaper outlines a comprehensive identity verification protocol designed for a new way of verification method to enable a better verification method for users on the internet regardless of their location or their device. This protocol will allow to confirm the identity of the person performing the transaction and without sharing of sensitive data or exposure of the critical details of the user.    
---

## Table of Contents

1. [Introduction](#introduction)

---

## Introduction

### The Challenge

Identity verification is either hard or can be done via others. You can send OTP SMS but if the phone is insecure then it does not allow safe handling of such measures. Also, every service/website/app needs to implement their verification mechanism and use providers. These providers do not use consistent method or define risk level or factors that they need to relay one. For example, for financial transactions they only use OTP via SMS. And they keep repeating the cycle for every transaction.

### Why This Matters

The identity is something very hard to confirm via an internet connection. The user can be anybody and the information can be faked and OTP and other methods like SMS are not secure way of communications. Although the mentioned methods are hard to penetrate there is still a high chance to not be able to confirm the identity.

This paper is trying to expand authentication and verification and provide a robust way to confirm the identity of the user doing the action. Not only limiting it to OTP method but expanding it and provide a secure connection and making sure the communication is secure and not being hacked or not the intended user is doing the action.

## IVP

IVP aims to verify the user identity via device. Regardless of the device being used, PC or Laptop or smart phone. We will link the unique identifier of the physical device to the user and make sure this is the real user. We aim to create more secure network communication via any network and allow the verification to be completed not only via the internet. The IVP is a free to use standard and to implement under the Apache 2.0 License with it's related conditions.

### IVP Elements

The IVP Contains the following elements:
1. Authenticated User: The user who is allowed to access the resources
2. Authenticated Device: The device that the user approve to do the action
3. IVP Provider: The provider that has a record for the Authenticated User and Authenticated Device and can confirm the identity.
4. Verification Methods: To confirm the identity there should be a challenge to the user requesting the service and upon successful confirmation of the challenge the user is confirmed or unsuccessful challenge will lead to denying the requestor of doing an action.
5. Confirmation Data: The data stored inside the IVP provider to confirm the user identity. Data should be only stored as a hash of type SHA512 with consideration of quantum proofing. No IVP provider to be listed as complied unless this requirement is met and the data of the user is not stored in plain text or a format that is accessible. The data represents the unique details for the user and the device for example user email and user device IMEI or BIOS Serial number.
6. Restriction Level: Is the user allowed or not allowed to do an action based on several factors, for example the user is only allowed to do the action if he inside a certain geographical location. Or from a certain IP or a inside a network.
7. Verification Level: How many confirmations did the user do and what is their level. For example, for a high security risk system the user must complete pin and email otp. In low risk actions an SMS otp is acceptable.
8. Session Connection: The user will have the session active and can do the actions on different systems as long as the session does not go out of expiry.


**Contact:** Advanced Software Solutions

**Email:** info[at]advancedsoftware.io

**Website:** https://advancedsoftware.io

---

*This document is a draft. Comments and feedback are welcome.*
