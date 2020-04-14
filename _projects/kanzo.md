---
layout: page
title: Kanzo
description: A platform to connect Agents, Tenants & Contractors to help speed up maintenance, inspections & inventories in the property rental industry.
---
This project started towards the end of 2019 with a friend after we realized how time consuming the process of getting 
something fixed in a rental property is. It typically involves emailing an agent, the agent then emailing a contractor, the 
contractor asking for more specific details to the agent, the agent emailing you again and so on. This seemed ridiculous and 
after doing some online market research, it seemed there wasn't a solution that allowed all parties involved to easily 
communicate in one platform efficiently. 

We then went to dozens of estate agents and began asking questions about the process and tried to understand to the best of 
our ability the problems that existed and then planned out potential solutions. 

This has been developed in both of our spare time and we are currently in an Alpha phase of the software, where we're actively
looking for companies to trial the software that exists so far so we can prepare for a more robust public beta.

The software was initially built as a pure Django project, but has since been decoupled in to a Django REST API (with DRF) and
the frontend being a React application. The infrastructure is currently hosted on Google Cloud platform with the aim to fully 
containerize and orchestrate deployment and scaling with Kubernetes. 
