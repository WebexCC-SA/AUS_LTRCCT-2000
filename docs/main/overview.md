---
#icon: material/folder-open-outline
icon: material/bullseye-arrow
---
<script>
    // Function to initialize and handle form submission
    function setupAttendeeForm() {
        const form = document.getElementById('attendee-form');
        const displayAttendee = document.getElementById('display-attendee');
        const attendeeInput = document.getElementById('attendee');

        // Load stored Attendee ID on page load
        const storedAttendeeID = localStorage.getItem('attendeeID');
        if (storedAttendeeID) {
            attendeeInput.value = storedAttendeeID;
            displayAttendee.textContent = storedAttendeeID;
        }

        // Restrict input to only allow three digits
        attendeeInput.addEventListener('input', function() {
            this.value = this.value.replace(/\D/g, '').slice(0, 3);
        });

        // Handle form submission
        form.addEventListener('submit', function(event) {
            event.preventDefault();
            const attendeeIDInput = attendeeInput.value;

            if (attendeeIDInput && attendeeIDInput.length === 3) {
                // Store the Attendee ID in local storage
                localStorage.setItem('attendeeID', attendeeIDInput);

                // Update the displayed Attendee ID
                displayAttendee.textContent = attendeeIDInput;
            } else {
                alert('Please enter exactly 3 digits.');
            }
        });
    }

    // Wait for the DOM content to be fully loaded
    document.addEventListener('DOMContentLoaded', setupAttendeeForm);
    
    document.addEventListener('DOMContentLoaded', function() {
        const attendeeID = localStorage.getItem('attendeeID') || 'Not Set';
        const attendeePlaceholder = document.getElementById('attendee-id-placeholder');

        if (attendeePlaceholder) {
            attendeePlaceholder.textContent = attendeeID;
        }
    });
</script>

<style>
    /* Style for the button */
    button {
        background-color: black;
        color: white;
        border: none;
        padding: 10px 20px;
        cursor: pointer;
    }

    /* Style for the input element */
    input[type="text"] {
        border: 2px solid black;
        padding: 5px;
    }
</style>

<!-- Markdown content with embedded HTML -->
<div>
    <h2>Please put in your Attendee ID into the box below and click Save.</h2> 
    <form id="attendee-form">
        <label for="attendee">Attendee ID:</label>
        <input type="text" id="attendee" name="attendee" placeholder="Enter 3 digits" required>
        <button type="submit">Save</button>
    </form>

    <br>

    <p>Your stored Attendee ID is: <b><span id="display-attendee">No ID stored</span></b></p>
    
<h3>All configuration entries in the lab guide will be renamed to include your Attendee ID.</h3>
</div>

# Overview
Building an AI agent is as easy as ordering flowers!
We will begin with building a voice Autonomous Agent that will help the caller order flowers for their partner. It could be an anniversary or other occasions. The agent will also capture email address, shipping address, offer choices etc.
We will get the agent to capture and store the booking in a database.
We will then hook it up the voice flow and interact with it.
We will also build Scripted AI Agent to do specific tasks like fetching status of the order.

## Learning Objectives <br><br>

 **• Integrate Intelligent AI Agents:** Utilize Cisco Autonomous and Scripted AI Agents to build dynamic, context-aware self-service flows that adapt to customer needs in real-time. <br><br>
**• Seamless AI-to-Human Collaboration:** Experience smooth transitions from AI agents to human agents, ensuring continuous context and interaction summaries for effective issue resolution. <br><br>

![Profiles](../graphics/NewLab/Overview/1.1.png)

## Use Case: Webex AI Agent Design - 4Flowers!

Designing a **Webex AI Agent** for 4Flowers, a flower shop, to assist callers to order flowers. This will solve the order capturing problem that the staff have to deal with and will give them time back to focus on higher value tasks like making the bouquets, for example. If our AI agent cannot accomplish the task, it will send the call to a human staff member along with the transcription.

### AI Agent Capabilities

- **Recommending flowers** based on customer preferences or occasions  
- **Collecting order details** for both **standard and custom bouquets**  
- **Calculating total price** in real time  
- **Gathering delivery information**, including **address**, **email**, and **sms number**.
- **Order Confirmation will be sent to the email that the contact provides (you can use your own email address) when interacting with the AI agent.**
    - We are using Gmail with OAuth 2.0 to send emails
    - This setup is not part of this lab but if you have questions, we can cover it after the lab.
    - [BONUS] SMS channel is something you can try on your Gold Tenants
- **Providing order status updates** upon request  
- **Sharing store hours** and relevant **business information**  
- **Transferring to a human agent** when needed - augmenting the human 
- **BONUS - not part of this lab**
    - Try including **delivery date**, **changing delivery location** - you may need to make changes to the MockAPI database and other related changes in the AI Agent and flows.
<!--### Human Agent Support

- **Human agents** are equipped with **AI-powered tools** to ensure:
  - **Fast issue resolution**  
  - **Personalized service**  
  - **Exceptional customer experience** across all interactions-->



## Disclaimer
The lab design and configuration examples provided are for educational purposes. For production design queries, please consult your Cisco representative or an authorized Cisco partner.
Let’s get started and discover how **Webex Contact Center** can transform your customer operations and experience with AI agents!

