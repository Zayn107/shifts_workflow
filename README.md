# Shift Management Workflow Automation

This project implements an automated shift management system using n8n, Telegram, and AI integration. The system processes shift requests through a Telegram bot and manages schedules using Google Drive.

## Features

- Telegram bot integration for receiving shift requests
- AI agent for processing and managing shift requests
- Google Drive integration for schedule storage
- Voice and text message support
- Automated schedule updates

## Prerequisites

- n8n instance running in the cloud
- Telegram Bot Token
- Google Drive API credentials
- OpenAI API key (for AI agent)

## Setup Instructions

1. **Telegram Bot Setup**
   - Create a new bot using BotFather on Telegram
   - Save the bot token securely

2. **Google Drive Setup**
   - Create a Google Cloud Project
   - Enable Google Drive API
   - Create service account credentials
   - Share the target Google Drive folder with the service account email

3. **n8n Configuration**
   - Import the workflow configuration from `workflow.json`
   - Configure the following credentials in n8n:
     - Telegram Bot Token
     - Google Drive Service Account
     - OpenAI API Key

4. **AI Agent Tools**
   - The AI agent has access to the following tools:
     - Schedule Viewer
     - Shift Request Processor
     - Conflict Detector
     - Schedule Updater

## Workflow Process

1. User sends a voice or text message to the Telegram bot
2. Message is processed by the AI agent
3. AI agent analyzes the request and current schedule
4. If approved, schedule is updated in Google Drive
5. User receives confirmation message

## File Structure

- `workflow.json` - n8n workflow configuration
- `agent_tools.json` - AI agent tool definitions
- `config.json` - Configuration settings

## Security Notes

- Keep all API keys and credentials secure
- Use environment variables for sensitive information
- Regularly rotate credentials
- Implement proper access controls in Google Drive 