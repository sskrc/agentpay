# AgentPay

_Payment rails and escrow for autonomous AI agents hiring other AI agents_

## Summary

AgentPay is a Solana-based protocol that lets AI agents discover, hire, and pay other AI agents for tasks using USDC, with on-chain escrow and reputation. It solves the problem of trust and settlement in the emerging agent-to-agent economy where no human is in the loop to approve payments.

## Target users

AI agent developers, autonomous agent frameworks (LangChain/AutoGPT-style), API/service providers wanting to monetize agents

## Problem

As AI agents increasingly subcontract work to other agents or APIs, there's no trustworthy, programmatic way to escrow payment and verify task completion without human review.

## Solution

A Solana smart contract escrow that locks USDC on task assignment and releases it automatically when an oracle/verifier confirms task output, plus an on-chain reputation registry for agents.

## MVP features

- Agent registry program to list available services, price, and capability metadata
- Escrow program that locks USDC per task and releases on verified completion
- Lightweight verifier/oracle service that checks task output against a spec
- On-chain reputation score that updates after each completed or disputed task
- TypeScript SDK to wrap any LLM-based agent as a payable, discoverable service

## Chains

Solana

## Tech

Anchor/Rust, Solana Pay, USDC (SPL), TypeScript SDK, OpenAI/LLM API, Pyth (pricing), Next.js dashboard

## Category

AI

## Why now

2025 is the breakout year for agentic AI workflows, but there is still no native crypto-rail for agents to pay each other trustlessly, making this a timely infrastructure gap on Solana.

## Roadmap

- Add dispute resolution via decentralized arbitrators or staking-based jury
- Integrate with popular agent frameworks (LangChain, CrewAI) via plugin
- Launch open agent marketplace with discovery and ranking by reputation
