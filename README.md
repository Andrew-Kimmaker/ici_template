# 🌟 Moo GPA Savior — "Homework Alarm" for NCCU Students

## Project Description
Moo GPA Savior is an automated deadline tracking and notification system built for NCCU students who struggle with disorganized Moodle email alerts and missed assignment deadlines. By connecting to the Moodle iCal API, the system extracts upcoming deadlines, generates real-time countdown metrics, and pushes organized task reminders directly to users via LINE Notify. An integrated AI chatbot powered by OpenAI API further allows students to query their deadlines conversationally in natural language.

This project addresses a real pain point in student academic life — cognitive overload from unstructured notification systems — and demonstrates how automation and AI can reduce academic stress and prevent late submissions.

## Getting Started

### Prerequisites
- Python 3.8+
- Google Colab (recommended) or Jupyter Notebook
- A Moodle account with iCal URL (from NCCU Moodle calendar export)
- A LINE Bot account with Messaging API access token
- An OpenAI API key

### Setup
1. Open `Final.ipynb` in Google Colab
2. Fill in your credentials in the configuration section at the top
3. Edit `MY_COURSES` to match your enrolled courses
4. Run all cells — the dashboard will launch automatically

## File Structure
ici_template/

├── Final.ipynb              # Main notebook: Moodle dashboard + LINE notify + AI chatbot

├── poster/

│   └── Moo_GPA_Savior.jpg   # Project poster presented May 28, 2026

└── README.md
## Analysis
The system was built and tested using real Moodle iCal data from NCCU's ICI program.

**Key components:**
- **Moodle iCal Parser** — extracts task names, deadlines, and countdown timers from the Moodle calendar export URL
- **LINE Notify Integration** — formats and pushes the top 5 upcoming tasks directly to the user's LINE app via the Messaging API
- **Interactive HTML Dashboard** — displays ongoing tasks, attendance logs, and archived deadlines in a tabbed UI rendered inside Google Colab
- **RAG-style AI Chatbot** — powered by OpenAI GPT-4o-mini, the chatbot is given the student's live task list and course list as context, enabling natural language queries like "What's due this week?" or "Which deadline is closest?"

## Results
- Successfully automated deadline extraction and real-time LINE push notifications
- Dashboard displays prioritized, color-coded task cards (urgent vs. in-progress)
- AI chatbot accurately responds to course and deadline queries in both English and Traditional Chinese
- System reduces manual Moodle checking and lowers student cognitive load

**Limitations:**
- Dependent on Moodle iCal export URL and LINE Messaging API availability
- OpenAI API usage incurs cost — not free to scale
- No persistent storage; resets each Colab session

## Contributors
| Name | Role |
|------|------|
| Andrew Kim | Project ideation, poster & presentation design, presenter |
| Solomon | Main concept development, core system coding |
| Peter | System coding & implementation |

## Acknowledgments
We would like to thank our Introduction to AI course instructor at NCCU's International College of Innovation (ICI) for guidance and support throughout this project.

## References
- [Moodle iCal Calendar Export](https://docs.moodle.org/en/Calendar_export)
- [LINE Messaging API Documentation](https://developers.line.biz/en/docs/messaging-api/)
- [OpenAI API Documentation](https://platform.openai.com/docs/)
- [NCCU ICI Template](https://github.com/advapplab/ici_template)
