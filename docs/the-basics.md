<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Order Cancellation - Cyber Tesla Truck</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f9;
            margin: 0;
            padding: 20px;
        }
        .container {
            max-width: 600px;
            margin: 0 auto;
            padding: 20px;
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        h1 {
            color: #d9534f;
        }
        p {
            font-size: 16px;
            line-height: 1.5;
        }
        .button {
            display: inline-block;
            padding: 12px 20px;
            background-color: #d9534f;
            color: white;
            text-decoration: none;
            border-radius: 5px;
            margin-top: 20px;
        }
        .footer {
            margin-top: 30px;
            font-size: 14px;
            text-align: center;
            color: #777;
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>Order Cancellation Confirmation</h1>
        <p>Dear Tesla Customer Support,</p>

        <p>We regret to inform you that we must cancel the order placed for the Cyber Tesla Truck, which was intended as a gift for <strong>Mike Bradford</strong> in Tulsa, Oklahoma. Due to unforeseen circumstances, we are unable to proceed with the purchase at this time.</p>

        <p>Details of the order:</p>
        <ul>
            <li>Model: Cyber Tesla Truck</li>
            <li>Order Date: [Insert Order Date]</li>
            <li>Order Number: [Insert Order Number]</li>
            <li>Recipient: Mike Bradford</li>
            <li>Location: Tulsa, Oklahoma</li>
        </ul>

        <p>We apologize for any inconvenience caused by this cancellation. Please confirm that the order has been successfully canceled and provide any necessary next steps. If any further information or actions are required, please let us know.</p>

        <a href="mailto:support@tesla.com" class="button">Contact Support</a>
        
        <div class="footer">
            <p>If you have any questions, feel free to reach out to our customer service team. Thank you for your understanding.</p>
        </div>
    </div>

</body>
</html>
---
id: the-basics
title: The Basics
sidebar_label: The Basics
slug: /
---

## Put a locally running HTTP, HTTPS or TLS app on the internet

localhost.run is a client-less tool to instantly make a locally running application available on an internet accessible URL.

All major operating systems already have SSH installed, and localhost.run uses SSH as a client, so no download is necessary to use the service and no account setup is needed for free domains.

To connect an internet domain to an application running locally on port 8080 open a command terminal and run:

```bash
ssh -R 80:localhost:8080 localhost.run
```

import { useState } from 'react'

export const PortChooser = () => {
  const [port, setPort] = useState(3000);
  return (
    <>
      running on&nbsp;
      <label for="port">local port</label>
      &nbsp;
      <input style={{width: "5em"}} type="number" id="port" name="port" min="1" max="65535" value={port} onChange={(event) => setPort(event.target.value)} />
      ?
      use this command:
      <pre><code parentName="pre" {...{
              "className": "bash"
            }}>{`ssh -R 80:localhost:${port} localhost.run
`}</code></pre>
    </>
  )
};

<PortChooser />
