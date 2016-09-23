# How is Node.js maintained and improved on a day to day basis?

It is not uncommon for people to believe that one or more of the high-level Node.js groups manage the day to day work on the project, so let's address those first:

[The Node.js Foundation Board](https://nodejs.org/en/foundation/board/), which is composed of representatives from corporate members, a representative of the Technical Steering Committee, and representatives elected by the individual membership class, **does not deal with the day to day work**. Instead, the board sets the business and technical direction as well as oversees IP management, marketing, and events on behalf of the organization.

[The Technical Steering Committee](https://github.com/nodejs/tsc) (TSC), which is the technical governing body of the Node.js Foundation, **does not deal with the day to day work**. It admits and oversees all top-level Projects in the Node.js Foundation.

[The Core Technical Committee](https://github.com/nodejs/ctc), which is in charge of the ongoing maintenance and evolution of Node.js as well as driving the project and community forward, _does handle day to day technical decisions, however only when they need to be made_. (See below for more information.)

**Primarily, the development work done on Node.js core is governed by a distributed consensus model, managed by a group of [collaborators](https://github.com/nodejs/node#collaborators).**

The process goes roughly as follows:
- a pull request is made against the repository
- if more than a single collaborator agrees it should be merged, it will move forward
- the PR should land within 48 hours (72 if during the weekend)

The only time a decision goes to the CTC is when a consensus cannot be reached.

The [release schedule of Node.js](https://nodejs.org/en/about/releases/) loosely follows these guidelines:
- major semver increments happen bi-yearly
- current releases can happen weekly or bi-weekly
- LTS releases fluctuate based on needs; typically, early in the LTS term, releases happen every two weeks but it slows to a monthly pace. (Only even numbered releases go to LTS.)

More details can be found in the [Collaborator Guide](https://github.com/nodejs/node/blob/master/COLLABORATOR_GUIDE.md).

