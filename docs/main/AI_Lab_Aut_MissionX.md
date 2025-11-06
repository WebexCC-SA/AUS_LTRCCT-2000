---
#icon: material/folder-open-outline
icon: material/medal
---


# Mission  Integrating the AI Agent with Flow for Voice Calls

## Mission overview
Your mission is to:

Integrate the AI Agent with the Voice Flow. 

### Task 1. Build WxCC voice flow with AI Agent. <span style="color: red;">**Mostly Read ONLY - flows have been created for you but not published**</span>

1. In Control Hub navigate to **Flows**, in the Search bar above the list, search for **<span class="attendee-id-container">AutonomousAI_Flow_2000_<span class="attendee-id-placeholder" data-prefix="AutonomousAI_Flow_2000_">Your_Attendee_ID</span><span class="copy" title="Click to copy!"></span></span>**

2. Towards the extreme right of your listed flow, click on the edit button to launch the flow in Flow Designer

3. Make sure the **Edit** mode at the top is set to **ON**. Then, click on the **Virtual Agent V2** select **Static Contact Center AI Config** on the right
    >
    > Select Contact Center AI Config as **Webex AI Agent (Autonomous)**
    >
    > Virtual Agent: **<span class="attendee-id-container"><span class="attendee-id-placeholder" data-suffix="_2000_AutoAI_Lab">Your_Attendee_ID</span>_2000_AutoAI_Lab<span   class="copy" title="Click to copy!"></span></span>**
    
    <span style="color: red;">Information ONLY</span> By default, the **Conversation Transcripts** setting is enabled in VirtualAgentV2 block.
    <details>![Profiles](../graphics/Lab1_AI_Agent/2.54.png)</details>


4. Click on the QueueContact block and choose the queue for your attendee ID **<span class="attendee-id-container"><span class="attendee-id-placeholder" data-suffix="_2000_Voice_Queue">Your_Attendee_ID</span>_2000_Voice_Queue<span   class="copy" title="Click to copy!"></span></span>**

5. Click on the **Play Music** block and choose **defaultmusic_on_hold_cisco_opus_no_1.wav**
    <details>![Profiles](../graphics/Lab1_AI_Agent/2.49_148.gif)</details>  

6. **Validate** and **Publish** Flow. In popped up window click on dropdown menu to select **Latest** label (**DO NOT** Select any other tag but only **Latest**), then click **Publish**.
    <details>![Profiles](../graphics/Lab1_AI_Agent/2.51.gif)</details>

7. Assign the Flow to your **Channel (Entry Point)** - Do this by first going to **Channel** > Search for your channel **<span class="attendee-id-placeholder">Your_Attendee_ID</span>_2000_Channel**.

8. Click on **<span class="attendee-id-placeholder">Your_Attendee_ID</span>_2000_Channel**
    <details>![Profiles](../graphics/Lab1_AI_Agent/2.52.png)</details>
9. In **Entry Point** Settings section change the following:

    > Routing Flow: **<span class="attendee-id-container">AutonomousAI_Flow_2000_<span class="attendee-id-placeholder" data-prefix="AutonomousAI_Flow_2000_">Your_Attendee_ID</span><span class="copy" title="Click to copy!"></span></span>**

    > Version Label: **Latest**

    > Music on Hold: **defaultmusic_on_hold.wav**

    <details>![Profiles](../graphics/Lab1_AI_Agent/2.53.gif)</details>

10. Dial Support Number assigned to your **<span class="attendee-id-placeholder">Your_Attendee_ID</span>_2000_Channel** to test the Autonomous AI Agent over a voice call. <span style="color: red;">When speaking the Email address and Delivery Address - use NATO phonetic alphabet like "A for Alpha, B for Bravo" etc.</span>
> **Note:** This Lab is being conducted in a classroom with more than a few attendees.  
> Environmental factors, such as background noise and other attendees speaking next to you, may affect the response accuracy.  
> For best results, it is **strongly recommended to use computer headphones**, if available.


### Task 2. Test Agent Handoff Configurations.

1. Click <a href="microsoft-edge:https://beta-desktop.wxcc-us1.cisco.com">Launch Agent Desktop in Edge</a>.
   Or you can copy paste this URL to the Edge browser's address bar: https://beta-desktop.wxcc-us1.cisco.com Use the same **Agent** credentials on your card. You will see another login screen with OKTA on it where you may need to enter the email address again and the password provided to you. 
2. Select **Desktop** endpoint option and choose the team. **<span class="attendee-id-container"><span class="attendee-id-placeholder" data-suffix="__2000_Team">Your_Attendee_ID</span>_2000_Team<span class="copy" title="Click to copy!"></span></span>**. Click **Submit**. Allow browser to access Microphone by clicking **Allow** on every visit.
3. Make your agent ***Available*** and you're ready to make a call.

    <details>![profiles](../graphics/Lab1/5-Agent_Login.gif)</details>

4. From the Webex app dial pad, dial the +1 US Number assigned to you. This should have already been mapped to your **<span class="attendee-id-placeholder">Your_Attendee_ID</span>_2000_Channel** channel, and during the conversation with the AI agent, ask to talk to a representetive or live agent. Just say "Can I speak to an agent?"
    <details>![Profiles](../graphics/Lab1_AI_Agent/2.54_148.png)</details>

5. With this setting enabled, the live agent can see the conversation details between the caller and the AI agent. Please check if you can view the IVR transcripts during your test calls with Agent Handoff. 
    <details>![Profiles](../graphics/Lab1_AI_Agent/2.55_148.gif)</details>


<p style="text-align:center"><strong>Congratulations, you have officially completed the Autonomous AI Agent lab! 🎉🎉 </strong></p>
