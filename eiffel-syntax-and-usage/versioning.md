<!---
   Copyright 2017 Ericsson AB.
   For a full list of individual contributors, please see the commit history.

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.
--->

# Versioning
In Eiffel, each individual event type is versioned independently. This version is declared by the __meta.version__ property (see [The Meta Object](./the-meta-object.md)) and follows the [Semantic Versioning 2.0.0](http://semver.org/spec/v2.0.0.html) format. The documentation of each event type lists the complete version history of that type, including links to commits introducing older versions of the type.

The independent versioning of event types, as opposed to a protocol-wide versioning scheme, was chosen for the greater flexibility and extensibility it affords. There are consequences, however, which are important to understand:
* Consumers must always be ready to receive event types which they are unable to parse: the event producer may be ahead of the consumer on one event type, but not another. Similarly, new and/or custom event types must be expected and handled.
* Backwards incompatible changes may not be introduced to the __meta.type__ and __meta.version__ properties, as these together form the key which allows the consumer to unlock the remainder of the event.

That being said, to facilitate compatibility and consistency, the Eiffel protocol as described in this repository is released in named and internally coherent _editions_. Each of these editions is represented as a GitHub [release](https://github.com/Ericsson/eiffel/releases). A history of Eiffel editions is available below.

| Edition   | Tag                                                 | Changes                                          |
| --------- | --------------------------------------------------- | ------------------------------------------------ |
| Arica  | _Reserved for future use._  | |
| Lyon  | _Reserved for future use._  | |
| Paris  | _Reserved for future use._  | |
| Agen  | _Reserved for future use._  | |
| Toulouse  | [edition-toulouse](../../../tree/edition-toulouse)  | Stepped major version of TERCC. Updated FLOW_CONTEXT link type, resulting in new minor version of all event types. |
| Bordeaux  | [edition-bordeaux](../../../tree/edition-bordeaux)  | Initial edition. |
