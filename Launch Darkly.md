Launch Darkly Writeup from a Security Students Viewpoint

<h1>Platform Readiness<h1>

During this module I'm focusing on these ideas: 
  -Understanding what project architechure means within Launch Darkly 
  -How to create both projects and environments withing Launch Darkly 
  -Learning what steps are involved in mapping services and applications to project environments
  -How can Launch Darkly help DevOps teams follow secure SDLC principles & practives

**PROJECT ARCHITECHTURE**

Key Term: Feature Flag : Also commonly reffered to as a 'feature toggle' always teams to toggle certain features within an environments 
on or off very quickly and not have to push new code. From a security standpoints I find this very interesting because it allows 
a team to be able to quickly disable a feature that may have a security risk the team may have not been aware of. They can remediate this issue 
push the code then re-toggle the feature after it has been properly resolved.

The way LaunchDarkly implements their feature flag management is 
what makes them so special. Feature management isnt limited to software developers either. 
It can be used across many teams (Sales/Marketing/Product Managers). Anyone team that uses CI/CD can benefit from Launch darklys flag 
management.

Projects and Environments 

**PROJECT**

-A project can contain both environments and feature flags
-Feature flags are unique to a project
	-These flags can have different states unique to their environment
-Facilitates feature flag collaboration through SDLC

**Environment**
-Flags,rules,users,segments belong to env.
-The ability to have production and test environments and toggle features on or off withing each env.




Flag Delivery Network Architechtre:

-Global CDN that run the Flag Delivery Network
	-I'd be interested to learn more about how the flag delivery architecture was built and what role the security team played in it.
	-Does the long lived connection introduce any security risks?
	-The ability to set rules is a really cool feature if you want to push out features to only certatin types of users(i.e filter by Mobile or Browswer devices).



**Authorization**

Key learning objectives 
	-Understand roles 
	-Understand how to implement roles depending on needs of an org.
	-Understand how to modify roles/ create custom roles/ assign permissions 


What are the built in roles? 
	-Reader,Writer,Admin,Owner

In terms of priviledge : Owner > Admin > Writer > Reader 
Roles are great to assign specific actions to specific users. Very cool that they have this option, from a security standpoint you always want to use role based access control if available.

I think its extremely useful that Launch Darkly documentation has guidelines on custom role creation to help orgs implement role based access responsibly.

Check in: 
Which risk(s) would a custom role be effective in mitigating? 
	-Compromised or malicious insider 
	-Member making changes to a platform that impacts the fidelity of running experiments
	
You've decided to create a custom role for your Tech Lead who is tasked with managing future releases, monitoring and approving flag changes, as well as delegating flag changes. Which permissions should you assign them?
	Yes: 
	-Create/Edit Flags
	-Toggle Flags On/Off
	-Approve Flag Changes 
	-Assign Reviewers
	-Archive Flags
	No: 
	-Create and Mangae Roles
	-Assign Roles to members 
	Use least priviledge when creating roles ! 

I'd really love to get my hands on the Launch Darkly console and be able to do some Role assignning lol 


<h1> Access<h1> 




