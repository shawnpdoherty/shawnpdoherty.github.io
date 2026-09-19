---
layout: post
title: "Stage 1: Power, Console, and Network"
date: 2026-09-19
---

The first stage of a usable hardware lab is not flashy. It is not automation for automation's sake. It is the foundation that makes everything else possible.

## The three essentials

When building a centralized hardware development environment, there are three things that must work before any higher-level workflow is trustworthy.

### 1. Power

Remote power control is the most important requirement. A Device Under Test(DUT) cannot be meaningfully tested if it cannot be powered cleanly, deterministically, and repeatedly.

This means being able to:

- power on the board
- power it off cleanly
- cycle power for a reset
- ensure the DUT arrives in a known state before the next test

Without this, the test environment is unpredictable.

### 2. Console

Serial console access is the second requirement. It gives visibility into the boot path and the early system state.

This is where you see:

- boot evidence
- device state transitions
- recovery paths
- failures before higher-level software layers are involved

If you cannot see the board during boot, you are effectively debugging blind.

### 3. Network reachability

Network access is the third essential, but it still matters. A reachable DUT can be tested, pinged, and integrated into the larger workflow.

This is the minimum health check for a device on the lab network.

## Why this matters

These three features are the baseline for any serious hardware workflow.

If any one of them is missing, the lab is still incomplete:

- no reliable power means no deterministic reset
- no console means no visibility
- no network reachability means no practical communication path

