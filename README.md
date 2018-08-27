# Enchanter
Lightweight workflow service based on state machine language.

# Goal
Enchanter aims to explore ways to easily create and run lightweight distributed workflows.

- **Simplicity:**  Stay simple in both web/internet application development and enterprise development scenarios
- **Flexibility:**  Deployed by integrating it directly into the application or on separate standalone servers. Easy to extend to support more communication protocols than HTTP between the client and server.
- **Scalability:**  Decentralized Services
- **Performance:**  
- **Reliability:**  Automatic retries if workflow failed.
- **Maintenability:** Monitoring and Alert.

# Proposed Design

To address the above goals, the following design decisions are proposed:

* Based on state machine language like AWS Step Function, with enhancements such as signal function.
* A distributed message queue is leveraged for state change notification. A simple message queue interface is designed to support multiple implementation/providers.  It's based on Redis as a default/reference implementation. 
* HTTP protocol is supported as default. Moreover, other protocols should be supported easily as a plugin/SPI implementation.
* MySQL for workflow process data persistence.
* Leader election with Redis for simpicity.(Zookeeper is a little overpower).
* Two different types of monitoring:
    * Individual Workflow Monitoring(IWM): Check the status of individual workflow and compensate it via some actions such as retries periodically.
    * Basic Monitoring&Analysis(BMA): Collect statistics for all the workflows in the scenario and alert based on the predefined rules. e.g., An alert would be raised if the number of workflow instance in START status exceed XXX.

Enchanter Architecture



# Quick Start

 
# Feature (TODO)

# Status
