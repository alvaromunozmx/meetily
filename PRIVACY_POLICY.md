# Meetily Privacy Policy

*Last updated: July 21, 2026*

## Our Privacy-First Commitment

Meetily is built on the principle that your meeting data should remain private and under your control. This privacy policy explains how we handle data in our open-source meeting assistant.

## Data Processing Philosophy

### Local-First Processing
- **Meeting transcription**: Processed entirely on your device using local Whisper models
- **Audio recordings**: Never transmitted to external servers
- **Meeting content**: Remains on your infrastructure
- **AI summaries**: Generated locally or through your chosen LLM provider

### Your Data Ownership
- You own all meeting data, transcripts, and recordings
- Data is stored locally on your device
- No vendor lock-in - export your data anytime
- Complete control over data retention and deletion

### Vocabulary (Beta)
The vocabulary is a list of names and terms you want transcribed right (and how
they are misheard). It stays on your computer: it is given to the local Whisper
model as context and used to correct transcripts locally. It is never sent to an
AI provider, not readable through the MCP server, and not part of analytics. When
you fix a word in a transcript, Meetily keeps the previous text so you can undo
the fix; it is deleted with the meeting.

### Voice Profiles (Optional, Beta)
Voice profiles let Meetily recognize a person you named in an earlier meeting and
suggest their name ("Sounds like Ana Ruiz?"). They are off by default and turned
on only through an explicit consent dialog.
- **What is stored**: a voiceprint — a list of numbers describing a voice, not a
  recording — for each person you choose to save, plus one per detected speaker of
  each meeting you run speaker identification on. Voiceprints are biometric data,
  mostly about the people you meet with.
- **When**: only with voice profiles turned on, and Meetily asks every time before
  saving or extending a person's profile. Suggestions are never used as a name
  until you confirm them — unless you turn on "Use strong voice matches
  automatically" (off by default): then a voice that clearly matches a saved
  profile is named and added to that profile without asking, marked "Matched by
  voice" so you can undo it.
- **Where**: only in the local database on your computer. Voiceprints are never
  uploaded, never sent to an AI provider, not included in exports, not readable
  through the MCP server, and not part of analytics.
- **Deleting**: delete one profile or all of them in Settings → Voice profiles, or
  when turning the feature off. "Delete all" also erases the per-meeting
  voiceprints and cleans the database backups Meetily keeps before updates. When
  deleting a meeting you choose whether the voice samples it contributed go too.
  Uninstalling the app does not remove its data folder
  (`~/Library/Application Support/com.meetily.ai` on macOS); delete it to remove
  everything.

## Usage Analytics

### What We Collect
Usage analytics is optional and off by default. When you choose to enable it, Meetily collects minimal, anonymized usage data:

**Application Usage:**
- Feature usage patterns (which tools you use most)
- Session duration and frequency
- Performance metrics (transcription success rates, error frequencies)
- UI interaction patterns (button clicks, navigation flows)

**Technical Metrics:**
- Application version and platform information
- Error logs and crash reports (anonymized)
- Performance benchmarks (processing times, resource usage)

### What We DON'T Collect
We never collect:
- ❌ Meeting content, transcripts, or recordings
- ❌ Personal information or identifiable data
- ❌ File names, meeting titles, or metadata
- ❌ Audio data or voice patterns
- ❌ Participant names or contact information
- ❌ LLM conversations or AI-generated content

### Why We Collect This Data
When enabled, analytics helps us with:
- **Product Quality**: Identifying and fixing bugs that impact user experience
- **Performance Optimization**: Understanding resource usage and system bottlenecks
- **Security**: Detecting potential security issues and vulnerabilities
- **Feature Development**: Making data-driven decisions about new features
- **Open Source Sustainability**: Ensuring the project meets user needs effectively

### Analytics Implementation
- **Provider**: PostHog (privacy-focused analytics platform)
- **Default**: Off by default; analytics starts only after you enable it in settings
- **Anonymization**: All data linked to generated user IDs only - no personal identification
- **Data retention**: 12 months maximum, then automatically deleted
- **Encryption**: All data encrypted in transit using industry-standard protocols
- **Location**: Data processed in accordance with PostHog's privacy policy
- **Access Control**: Strictly limited to core development team members

## Third-Party Services

### LLM Providers (Optional)
If you choose to use external LLM providers, your meeting transcripts and
summary prompts are sent to that provider for processing. The app asks for
your explicit confirmation the first time you select each cloud provider:
- **Anthropic Claude**: Subject to Anthropic's privacy policy
- **OpenAI**: Subject to OpenAI's privacy policy
- **Google Gemini**: Subject to Google's privacy policy
- **Groq**: Subject to Groq's privacy policy
- **OpenRouter**: Subject to OpenRouter's privacy policy
- **Custom OpenAI-compatible server**: Subject to the policies of whoever operates that server
- **Built-in AI / Local Ollama**: Processed entirely on your device; nothing is transmitted

### Analytics Service (Optional)
- **PostHog**: Used for usage analytics when enabled
- **Data**: Only anonymized usage patterns, no meeting content
- **Control**: Completely optional, off by default, and user-controlled

## Your Privacy Rights

### Data Control
- **Access**: View all data stored locally on your device
- **Export**: Export your data in standard formats
- **Delete**: Remove all data from your device


### Analytics Transparency
- **Open source**: Full analytics implementation available for review in our source code
- **Opt-in**: New and existing installs have analytics disabled until you turn it on
- **Questions**: Contact us for any analytics-related concerns

## Data Security

### Local Security
- Meeting data (audio recordings, transcripts, summaries) is stored on your
  device in your user profile, protected by standard file system permissions
- The app does not add its own encryption layer on top; at-rest protection
  relies on your operating system's disk encryption (FileVault on macOS,
  BitLocker on Windows, LUKS on Linux) — we recommend keeping it enabled
- Meeting content is never transmitted unless you configure a cloud LLM
  provider, in which case transcripts are sent to that provider only after
  your explicit confirmation
- Provider API keys are stored in your operating system's credential store
  (Keychain / Credential Manager / Secret Service), not in the app database

### Open Source Transparency
- Full source code available for security review
- Community-audited privacy implementations
- No hidden data collection or tracking

## Changes to This Policy

We will notify users of any material changes to this privacy policy through:
- Updates to this document in our GitHub repository
- Release notes for application updates
- In-app notifications for significant privacy changes

## Recording Consent

Meetily records meetings **at your direction** — you are the data controller of your
recordings. Recording-consent laws vary by jurisdiction (several U.S. states require
the consent of all participants, and Mexico penalizes recording conversations you are
not part of). Always inform participants that a meeting is being recorded and obtain
their consent. See the **Legal Notice** in the app's About screen and in the README
for details. Meetily's output is not an official or legal record.

## Contact Us

For privacy-related questions or concerns about this distribution of Meetily:
- **GitHub Issues**: [Create an issue](https://github.com/alvaromunozmx/meetily/issues)

Meetily is a fork of the open-source [meeting-minutes](https://github.com/Zackriya-Solutions/meeting-minutes)
project by Zackriya Solutions; for questions about the upstream project, see their repository.

## Open Source Commitment

As an open-source project under MIT license, you can:
- Review our complete privacy implementation
- Modify data handling to meet your requirements
- Deploy entirely on your own infrastructure
- Contribute to privacy improvements

---

*This privacy policy applies to Meetily v0.0.5 and later versions. For enterprise deployments, additional privacy controls may be available.*
