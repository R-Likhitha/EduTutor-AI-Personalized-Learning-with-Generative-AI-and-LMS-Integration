---
title: EduTutorAI
emoji: 🐢
colorFrom: indigo
colorTo: pink
sdk: gradio
sdk_version: 5.34.2
app_file: app.py
pinned: false
license: apache-2.0
short_description: Personalized Learning with Generative AI
---

Check out the configuration reference at https://huggingface.co/docs/hub/spaces-config-reference
# 🎓 EduTutor AI - Complete Learning Platform

**An advanced AI-powered educational platform that provides personalized tutoring, homework analysis, interactive quizzes, and comprehensive progress tracking.**

## ✨ Features

### 🤖 AI Chat Tutor
- **Intelligent Responses**: Powered by IBM Granite 3.3 2B Instruct model with GPT-2 fallback
- **Multi-Subject Support**: Mathematics, Physics, Chemistry, Biology, and General topics
- **Difficulty Levels**: Beginner, Intermediate, and Advanced content
- **Math Problem Solving**: Automatic detection and step-by-step solutions for algebraic equations

### 📊 Advanced Homework Analyzer
- **Multi-Problem Detection**: Automatically identifies and separates individual problems
- **Comprehensive Solutions**: Detailed step-by-step solutions with explanations
- **Subject-Specific Analysis**: Tailored approaches for different academic subjects
- **Performance Assessment**: Grading estimates and improvement recommendations

### 📝 Interactive Quiz System
- **Dynamic Question Generation**: Creates subject-specific quizzes on any topic
- **Immediate Feedback**: Detailed explanations for each answer
- **Performance Tracking**: Automatic score calculation and analysis
- **Customizable Length**: 3-10 questions per quiz

### 📋 Study Plan Generator
- **Personalized Learning Paths**: Custom study plans based on topic and duration
- **Structured Modules**: Organized learning with time estimates and difficulty levels
- **Essential Terminology**: Key terms and definitions for each subject
- **Progress Milestones**: Clear goals and assessment points

### 📈 Progress Tracking
- **Comprehensive Analytics**: Detailed performance reports and trends
- **Multi-Student Support**: Track progress for multiple learners
- **Achievement System**: Badges and milestones for motivation
- **Learning Insights**: Personalized recommendations based on performance data

## 🚀 Quick Start

### Prerequisites
- Python 3.8 or higher
- CUDA-compatible GPU (optional, for better performance)
- Hugging Face account (optional, for access to more models)

### Installation

1. **Clone or download the application files**
   \`\`\`bash
   # Ensure you have app.py in your working directory
   \`\`\`

2. **Install dependencies**
   \`\`\`bash
   pip install -r requirements.txt
   \`\`\`

3. **Set up Hugging Face token (optional)**
   - Create a Hugging Face account at https://huggingface.co
   - Generate an access token
   - Set it as an environment variable or add to Google Colab secrets:
   \`\`\`bash
   export HF_TOKEN="your_token_here"
   \`\`\`

4. **Run the application**
   \`\`\`bash
   python app.py
   \`\`\`

5. **Access the web interface**
   - Open your browser and go to `http://localhost:7860`
   - The application will also provide a public Gradio link for sharing

## 🎯 How to Use

### AI Chat Tutor
1. Select your subject and difficulty level
2. Type your question in the chat input
3. Get instant, detailed responses with explanations
4. Ask follow-up questions for deeper understanding

**Example Questions:**
- "Solve 2x + 5 = 15"
- "What is photosynthesis?"
- "Explain Newton's first law"
- "How do I factor x² - 5x + 6?"

### Homework Analyzer
1. Select the subject of your homework
2. Paste your homework problems in the text area
3. Click "Analyze Homework" for comprehensive solutions
4. Review detailed explanations and study recommendations

### Interactive Quizzes
1. Enter a topic and select subject
2. Choose the number of questions (3-10)
3. Answer all questions using the radio buttons
4. Submit to see results with explanations

### Study Plans
1. Enter the topic you want to study
2. Select subject and study duration
3. Get a personalized learning roadmap with:
   - Structured modules and timelines
   - Key concepts and terminology
   - Study tips and resources

### Progress Tracking
1. **Add Progress**: Record completed activities with scores
2. **View Reports**: Generate comprehensive progress analytics
3. **Track Trends**: Monitor improvement over time
4. **Get Recommendations**: Receive personalized study advice

## 🧠 AI Models and Technology

### Primary Model
- **IBM Granite 3.3 2B Instruct**: Advanced language model optimized for educational content
- **Automatic Fallback**: GPT-2 model ensures reliability if primary model fails
- **GPU Acceleration**: CUDA support for faster response times

### Knowledge Base
- **Curated Content**: Expert-verified information across multiple subjects
- **Structured Learning**: Organized concepts with definitions and applications
- **Real-World Connections**: Practical applications and examples

### Math Solver
- **Algebraic Equations**: Step-by-step solutions with verification
- **Arithmetic Operations**: Order of operations and detailed calculations
- **Error Handling**: Helpful guidance when problems can't be solved automatically

## 📚 Supported Subjects

### Mathematics
- Algebra (linear equations, quadratics, systems)
- Geometry (shapes, area, volume)
- Calculus (derivatives, integrals, limits)
- Statistics (data analysis, probability)

### Physics
- Mechanics (motion, forces, energy)
- Thermodynamics (heat, temperature, entropy)
- Electromagnetism (electric and magnetic fields)
- Waves (sound, light, frequency)

### Chemistry
- Organic Chemistry (carbon compounds, reactions)
- Inorganic Chemistry (metals, salts, acids/bases)
- Chemical Bonding (ionic, covalent, molecular)

### Biology
- Cell Biology (organelles, processes)
- Genetics (DNA, inheritance, mutations)
- Photosynthesis and Respiration
- Ecology and Evolution

## 🔧 Configuration

### Environment Variables
- `HF_TOKEN`: Hugging Face API token for model access
- `CUDA_VISIBLE_DEVICES`: GPU selection for CUDA acceleration

### Model Configuration
The application automatically detects available hardware and configures models accordingly:
- **GPU Available**: Uses CUDA acceleration with float16 precision
- **CPU Only**: Falls back to CPU processing with float32 precision

## 📊 Performance and Scalability

### System Requirements
- **Minimum**: 4GB RAM, 2GB storage
- **Recommended**: 8GB RAM, 4GB storage, CUDA-compatible GPU
- **Optimal**: 16GB RAM, 8GB storage, modern GPU (RTX 3060 or better)

### Response Times
- **With GPU**: 1-3 seconds for most queries
- **CPU Only**: 5-15 seconds depending on complexity
- **Simple Math**: Near-instantaneous regardless of hardware

## 🛠️ Troubleshooting

### Common Issues

**Model Loading Fails**
- Check internet connection for model download
- Verify sufficient disk space (2-4GB required)
- Try running with CPU-only mode

**Slow Performance**
- Enable GPU acceleration if available
- Reduce concurrent users
- Consider using lighter models for deployment

**Quiz/Progress Features Not Working**
- Ensure all form fields are filled correctly
- Check that scores are between 0-100
- Verify student names don't contain special characters

### Getting Help
- Check the console output for detailed error messages
- Ensure all dependencies are installed correctly
- Try restarting the application if issues persist

## 🤝 Contributing

This educational platform is designed to be extensible and customizable:

### Adding New Subjects
1. Extend the `KnowledgeBase` class with new subject data
2. Add subject-specific question templates for quizzes
3. Update the Gradio interface dropdown options

### Improving AI Responses
1. Enhance the knowledge base with more detailed content
2. Add new prompt templates for different question types
3. Implement additional fallback response strategies

### Adding Features
1. Create new methods in the `EducationalFeatures` class
2. Add corresponding Gradio interface components
3. Update the main application class to integrate new features

## 📄 License

This project is designed for educational purposes. Please ensure compliance with:
- Hugging Face model licenses
- Gradio usage terms
- Educational fair use guidelines

## 🙏 Acknowledgments

- **Hugging Face**: For providing the transformer models and libraries
- **Gradio**: For the excellent web interface framework
- **IBM**: For the Granite model series
- **SymPy**: For mathematical computation capabilities
- **PyTorch**: For deep learning infrastructure

## 📞 Support

For technical support or questions:
1. Check the troubleshooting section above
2. Review the console output for error details
3. Ensure all requirements are properly installed
4. Consider hardware limitations for performance issues

---

**EduTutor AI - Empowering Education Through Artificial Intelligence** 🎓✨
