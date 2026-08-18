# Proof of Concept: QR Code Check-in System

## Overview

This repository contains a lightweight Proof of Concept (PoC) developed in vanilla HTML5, CSS3, and JavaScript. The objective of this prototype is to evaluate the feasibility of client-side QR code generation and real-time camera-based decoding within modern web browsers without backend dependencies.

## Key Features

- **Client-Side QR Code Generation:** Dynamically renders unique QR codes representing event identifiers.
- **In-Browser Video Stream Capture:** Utilizes the WebRTC MediaStream API via `Html5Qrcode` to access available camera devices (`facingMode: "environment"`).
- **Real-Time Decoding & Event Mapping:** Captures frame buffers, decodes payload strings, and maps identifiers to predefined event entities in real time.
- **Extensibility:** Includes placeholder routines for asynchronous payload dispatch via the Fetch API (`POST`).

## Architecture & Dependencies

The prototype loads all third-party libraries via CDN:

| Library | Version | Purpose | Source |
| :--- | :--- | :--- | :--- |
| **Html5-QRCode** | Latest | Camera access and real-time QR code scanning/decoding | Unpkg CDN |
| **QRCode.js** | 1.0.0 | Dynamic client-side DOM injection of QR code SVGs/canvases | Cloudflare CDN |

## Project Structure

```text
.
└── index.html        # Single-file implementation containing markup, styling, and script logic
