# Specs

Ideally, we follow the idea of the top being the summary of the features below it  
*Eg, Scenarios are built using Personas, Agents, Scorecards and Simulations are the result of it*

*Test*  
[**Scenarios**](#scenarios)  
[Personas](#personas)  
[Schedules](#schedules)  
[Simulations](#simulations)

*Observe*  
	[**Analytics**](#analytics)  
	[Live Calls](#heading)  
	[Call Logs](#call-logs)  
	[Alerts](#alerts)  
	[Scorecards](#heading=h.ky7msgs0hhwr)

*Optimize*  
	[**Agents**](#agents)  
	[Prompts](#prompts)  
	[Tools](#tools)  
	[Fine Tuning](#fine-tuning)

## Scenarios {#scenarios}

**Scenarios** consist of a situation (base scenario prompt) that will happen between a group of **Personas** X **Agents**, resulting in **N** simulations, where **N** is the number of combinations of **Personas** and **Agents** (eg, 2 *Personas* and 5 *Agents* \= 10 *Simulations*)

The key aspects of **Scenarios** are	

* *Name*  
* *Prompt*  
* *Prompt Variables*  
  * *Name*  
  * *Type*  
  * *Default Value*  
* *Personas (Many, at least one)*  
* *Target Agents (Many, at least one)*  
* *Scorecard (1)*  
* *Schedule*

Scenarios can have different periodicities

* *Once (could be re-run manually, and will start the run at the moment it is created)*  
* *Daily*  
* *Weekly*  
* *Monthly*

*Period end conditions*

* *Never*  
* *End Date*  
  * *Requires an End Date value*  
* *After N amount of Runs*  
  * *Requires the value for number of runs*

To get the full scenario prompt, we should merge the **Scenario prompt** with the **Persona prompt**.

## Personas {#personas}

Personas are simplified customer behaviors (eg Angry Karen)

The key aspects of **Persona** are

* *Name*  
* *Language*  
* *Prompt*  
* *Mood (used as tags where applicable)*  
* *Background noise*

## Schedules {#schedules}

Schedules are programmed runs of the simulations, which can be updated in the Scenarios  
They can be disabled, so, if there is a scheduled simulation, it will be skipped until it is turned back on again.

The key aspects of **Schedules** are

* *Name (from the Scenario)*  
* *Periodicity*  
* *Last run date*  
* *Next run date, based on the previous run*  
* *Amount of runs*  
* *Active*




## Simulations	 {#simulations}

## **Simulations** are the result of the Scenario runs, in there, we can check what occurred during the test

## The key aspects of **Simulations** are

* ## *Name (Scenario\_Persona\_Agent\_Timestamp)*

* ## *Audio*

* ## *Transcription*

* ## *Analysis*

* *Score*  
* *Status (completed, in-progress, scheduled)*  
* *Date*

## 

## Analytics {#analytics}

**Analytics** is the main dashboard, where users can check results from **Simulations**, check **Alerts**, see how many **ongoing calls** are happening and data regarding **agent improvements** overall.

The key aspects of **Analytics**  are

* **Simulations** and their averages  
  * Number of runs	  
  * Average score between runs  
* **Alerts** and their averages  
* **Calls** and their averages  
* **Agent Performance** and their averages

## 	 {#heading}

## Live Calls

**Live calls** is where we can monitor and take action on ongoing calls, as well as listen to them  
There, we can take some actions, like **Listen**, **Transfer** or even **End Call**.

The key aspects of **Live Calls** are

* *From (Phone number)*  
* *To (Phone number)*  
* *Demands some action (Based on alerts listening to the call)*  
* *Origin (either Simulation, or real call (need a better name for it)*

## Call Logs {#call-logs}

**Call logs** is where we can check previous calls that happened, (*including simulations*)  
We can **run analysis** on them, to gather extra information on **improvement** possibilities

The key aspects of **Call Logs** are

* *Source (VAPI, Bland, etc)*  
* *From (Phone number)*  
* *To (Phone number)*  
* *Date*  
* *Score (If it was run through analysis)*  
* *Analysis*  
* *Audio*  
* *Transcript*

## 

## Alerts {#alerts}

**Alerts** are a way for the users to keep track of out-of-the-ordinary information and behaviors that can happen during a call. They can be used to keep track of how compliant an agent is with some important information.

The key aspects of **Alerts** are

* *Name*  
* *Trigger condition (prompt explanation of what to look for in the calls)*  
* *Where to send the notifications (SMS, email, slack, etc)*

## 

## Scorecards

**Scorecards** is our main way of evaluating the quality of a call, based on a set of **Categories** with their **Criteria**.  
They can be attached to a **Scenario**, or to a **Call** in the **Call Logs**.

The key aspects of **Scorecards** are

* *Name*  
* *Description*  
* *Categories (Many, at least one)*  
  * *Name*  
  * *Weight (0-100%, cannot surpass 100%)*  
  * *Criteria (Many, at least one)*  
    * *Name*  
    * *Weight (0-100%, cannot surpass 100%)*  
    * *Type (Yes/No, Quantity, etc)* 

## 

## Agents {#agents}

**Agents** are the focus of the product, where we aim to improve their prompts and models.  
They are fetched from their providers (eg VAPI, Bland, etc)

The key aspects of **Agents** are

* *Name*  
* *Prompt*  
* *Tools*  
* *Model*  
  * *Provider*  
  * *Model*  
  * *Temperature*  
  * *Tokens*


## 

## Prompts {#prompts}

**Prompts** is where we can keep a library of all available agent-prompts for a workspace, we can also have a predefined library of our own, based on the highest scoring prompts overall

The key aspects of **Prompts** are

* Name  
* Prompt  
* Tags

## 

## Tools {#tools}

Tools is where we can keep track of the actions the agent can take during the call

The key aspects of **Tools** are

* Name  
* Type (API Request, MCP, Routing, etc)

## 

## Fine Tuning {#fine-tuning}

Fine-tuning is our unique angle on the main issue we are going to solve, the idea is to gather feedback from calls, and transform that into data for the models to be trained on.

The key aspects of **Fine Tuning** are

* Training data, which comes from calls and their feedbacks (positive and negative, and insights on what could have been improved)

		  
	

