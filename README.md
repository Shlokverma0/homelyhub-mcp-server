# HomelyHub MCP Server

A Python MCP (Model Context Protocol) server that exposes the HomelyHub property-booking REST API as tools an LLM can call.

## Tools
- `list_properties`: lists available stays. Use when the user asks for places to stay.
- `property_details`: returns details of one property by ID.

## Features
- Clear tool descriptions so the LLM knows when to use each tool
- Handles HTTP errors, network failures and timeouts with httpx
- Tested with MCP Inspector

## Run
pip install -r requirements.txt
mcp dev server.py

## Note
The backend runs on a free tier, so the first request may be slow while it wakes up.

## Tech
Python, MCP (FastMCP), httpx, REST API
