# LLM Feedback SDK

[![Maven Central](https://img.shields.io/maven-central/v/io.github.interfish418/llm-feedback)](https://search.maven.org/artifact/io.github.interfish418/llm-feedback)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

An Android SDK that enables seamless integration of AI-powered feedback collection in mobile applications.

## Features

- 🎯 **Smart Feedback Collection**: AI-powered feedback analysis and categorization
- 🎤 **Voice Input Support**: Built-in speech-to-text functionality
- 💬 **Conversational Interface**: Natural language interaction for better user engagement
- 📊 **Real-time Analytics**: Instant feedback processing and insights
- 🎨 **Customizable UI Components**: Pre-built components that match your app's design
- 🔒 **Privacy-First**: Secure data handling and user privacy protection

## Installation

Add the dependency to your app's `build.gradle` file:

```gradle
dependencies {
    implementation 'io.github.interfish418:llm-feedback:1.0.0'
}
```

## Quick Start

### Basic Setup

```kotlin
import com.example.llm_feedback.*

class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        
        // Initialize the SDK
        LLMFeedback.initialize(this)
        
        // Show feedback dialog
        FeedbackCard.show(this) { feedback ->
            // Handle feedback result
            println("Received feedback: $feedback")
        }
    }
}
```

### Voice-Enabled Feedback

```kotlin
// Enable voice input for feedback collection
val voiceComponent = WaveformBarVoiceInputComponent(this)
voiceComponent.setOnFeedbackReceivedListener { audioFeedback ->
    // Process voice feedback
    handleVoiceFeedback(audioFeedback)
}
```

### Custom Rating Component

```kotlin
// Use built-in emoji rating component
val ratingComponent = EmojiRatingComponent(this)
ratingComponent.setOnRatingChangedListener { rating ->
    // Rating from 1-5
    submitRating(rating)
}
```

## Configuration

### API Keys

Add your API keys to `local.properties`:

```properties
google.api.key=YOUR_GOOGLE_API_KEY
openai.api.key=YOUR_OPENAI_API_KEY
```

### Permissions

Add these permissions to your `AndroidManifest.xml`:

```xml
<uses-permission android:name="android.permission.RECORD_AUDIO" />
<uses-permission android:name="android.permission.INTERNET" />
```

## Requirements

- Android API level 24 (Android 7.0) or higher
- Kotlin support
- Internet connection for AI processing

## Documentation

For detailed documentation and advanced usage examples, visit our [documentation site](https://github.com/interfish418/llm-feedback/wiki).

## Support

If you encounter any issues or have questions:

- 📧 Email: interfish@zohomail.com
- 🐛 [Report a bug](https://github.com/interfish418/llm-feedback/issues)
- 💡 [Request a feature](https://github.com/interfish418/llm-feedback/issues)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Changelog

### v1.0.0
- Initial release
- Core feedback collection functionality
- Voice input support
- Customizable UI components
- AI-powered feedback analysis

---

Made with ❤️ for Android developers
