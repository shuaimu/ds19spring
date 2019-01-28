

# Course introduction

## Class stuff and office hour

* Lecturer: Shuai Mu shuai@cs.stonybrook.edu
* Office hour: 2:30-3:30pm M F
* TA TBD

## Prerequisites

* Familiar with OS & networking
* Substantial programming experience 
* Comfortable with concurrency and threading

## Polling of PhD and Master 

## Course readings

* Lectures are based on research papers
* Check webpage for schedules
* Lectures assume you have read the assigned papers
* No textbook

## Important addresses

* class schedule
* piazza 

## How are you evaluated? (tentative)

* Labs 35% 
* Mid-term 25%
* Final 35%
* Participation 5%

## Lab policies

* You must work alone on all assignments
* Late policy: 20% off per day  

## Integrity policies 

* The work that you turn in must be yours
* You must acknowledge your influences
* You must not look at, or use, solutions from prior years or the Web, or seek assistance from the Internet
* You must take reasonable steps to protect your work
* You must not publish your solutions
* If there are inexplicable discrepancies between exam and lab performance, we will over-weight the exam and interview you.

## What are distributed systems?

* Machines communicate to provide some service for applications
* Multiple hosts
* A local or wide area network


## Why distributed systems?

* ease-of-use (web, NFS)
* availability/reliability (hardware/software failures)
* scalable capacity (CPU, memory, storage)
* modular functionality (authentication service)

## Downside
* A distributed system is a system in which I can’t do my work because some computer that I’ve never even heard of has failed.” -- Leslie Lamport

## Main challenges/topics in distributed systems

* Abstraction/Interface
 * different system requirements: file system/database/disk 
 * simple, flexible, implementation-friendly
* System architecture
 * data center / wide area
 * client-server / peer-to-peer
* Fault Tolerance
 * backup/replication
 * backup fail-over 
* Consistency
 * keep replicas identical
 * keep replicas non-idential
* Performance
 * throughput (parallelism/divide load)
 * latency (queuing, minimize critical path)
