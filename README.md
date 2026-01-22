# QA Manual Testing - Shelf Link

## 📚 Project Overview

**Shelf Link** is a digital book management application that allows users to organize, track, and manage their personal book collections. Users can create virtual bookshelves, categorize books by reading status, track reading progress, and maintain a comprehensive library of their reading journey.

### Key Features
- User authentication and profile management
- Book catalog management (add, edit, delete, search)
- Custom shelf organization
- Reading status tracking (Want to Read, Currently Reading, Read)
- Book details and metadata management
- User-friendly interface for book discovery and organization

---

## 🎯 Scope of Testing

This QA testing project focuses on comprehensive manual testing of the Shelf Link application's core functionality. The testing scope includes:

### In Scope:
- **User Authentication**: Registration, login, logout, password management
- **Book Management**: CRUD operations for books (Create, Read, Update, Delete)
- **Shelf Organization**: Creating, managing, and organizing custom shelves
- **Search Functionality**: Book search and filtering capabilities
- **Reading Status Tracking**: Updating and managing book reading statuses
- **User Profile Management**: Profile updates, settings, and preferences
- **Input Validation**: Form validations and data integrity checks
- **Security Testing**: Basic authentication, authorization, and input sanitization
- **Usability Testing**: User experience and interface consistency

### Out of Scope:
- Performance and load testing
- Automated testing implementation
- API testing (backend only)
- Database integrity testing at the infrastructure level
- Third-party integrations (e.g., external book APIs)
- Mobile application testing (if separate from web)
- Accessibility testing (WCAG compliance)

---

## 🔍 Testing Approach

This project follows a **Requirement-Based Testing** approach to ensure comprehensive coverage of all functional requirements.

### Methodology:
1. **Requirements Analysis**: Thoroughly review and analyze application requirements and user stories
2. **Test Planning**: Define test strategy, scope, and resource allocation
3. **Test Design**: Create detailed test scenarios and test cases based on requirements
4. **Test Execution**: Execute test cases manually, document results
5. **Defect Reporting**: Log bugs with detailed reproduction steps and supporting evidence
6. **Regression Testing**: Re-test fixed bugs and verify no new issues introduced

### Test Documentation Structure:
```
qa-manual-testing-shelf-link/
├── 01_Test-Scenarios/        # High-level test scenarios
├── 02_Test-Cases/             # Detailed step-by-step test cases
├── 03_Negative-Test-Cases/    # Error handling and boundary tests
├── 04_Bug-Reports/            # Documented defects and issues
└── README.md                  # Project documentation (this file)
```

### Test Case Categories:
- **Positive Test Cases**: Verify expected behavior with valid inputs
- **Negative Test Cases**: Verify error handling with invalid inputs
- **Boundary Test Cases**: Test limits and edge cases
- **Security Test Cases**: Verify authentication, authorization, and data protection

### Tools & Techniques:
- Manual exploratory testing
- Equivalence partitioning for input validation
- Boundary value analysis
- Error guessing for negative scenarios
- Test case documentation in Markdown format

---

## ⚠️ Known Limitations

### Testing Limitations:
1. **Limited Test Environment**: Testing conducted in staging environment only; production environment not accessible
2. **Test Data Constraints**: Limited test data availability; using synthetic data for most scenarios
3. **Time Constraints**: Full regression testing not always feasible within sprint timelines
4. **Browser Coverage**: Testing primarily on Chrome and Firefox; limited Safari and Edge testing
5. **Device Coverage**: Testing focused on desktop browsers; mobile responsive testing limited
6. **No Automation**: All tests are manual, which limits regression test frequency

### Application Limitations (Known Issues):
1. **Session Management**: Intermittent session timeout issues during login (see BUG-001 in `04_Bug-Reports/`)
2. **Search Performance**: Search becomes slow with large book collections (500+ books)
3. **File Upload Size**: Profile picture upload limited to 2MB
4. **Browser Compatibility**: Minor UI inconsistencies in older browser versions
5. **Concurrent Users**: Potential data sync issues when multiple users edit same book simultaneously

### Documentation Limitations:
1. Some edge cases may not be documented yet
2. API-level testing not included in current documentation
3. Performance benchmarks not established
4. Accessibility test cases not defined

---

## 🎓 What I Learned as a QA

### Technical Skills:
- **Test Case Design**: Learned how to write clear, detailed, and reproducible test cases that cover both happy paths and edge cases
- **Negative Testing**: Gained expertise in thinking like an attacker and testing security vulnerabilities (SQL injection, XSS)
- **Bug Reporting**: Developed skills in writing comprehensive bug reports with clear reproduction steps, expected vs. actual behavior, and supporting evidence
- **Test Documentation**: Learned the importance of well-organized, maintainable test documentation using Markdown
- **Requirement Analysis**: Improved ability to analyze requirements and identify testable scenarios

### QA Best Practices:
- **Think Like a User**: Always consider the end-user perspective and real-world usage scenarios
- **Question Everything**: Don't assume anything works; verify all functionality thoroughly
- **Document Everything**: Clear documentation is crucial for knowledge transfer and future reference
- **Reproduce Before Reporting**: Always verify bugs are reproducible before logging
- **Test Early, Test Often**: Early testing helps catch issues before they become expensive to fix

### Domain Knowledge:
- **Book Management Systems**: Understanding of how digital library systems organize and manage content
- **User Authentication Flows**: Learned common authentication patterns and security considerations
- **Data Validation**: Importance of input validation for both functionality and security

### Soft Skills:
- **Attention to Detail**: QA requires meticulous attention to small inconsistencies and edge cases
- **Critical Thinking**: Ability to identify potential issues before they occur
- **Communication**: Clear communication with developers about bugs and requirements
- **Patience and Persistence**: Thorough testing requires patience to execute repetitive tests
- **Adaptability**: Being flexible when requirements change or new features are added

### Key Takeaways:
1. **Quality is Everyone's Responsibility**: QA testing is not just about finding bugs, but ensuring the entire team delivers quality
2. **User Empathy**: Understanding user needs helps identify what truly matters in testing
3. **Continuous Learning**: Technology and testing practices evolve; staying updated is essential
4. **Balance**: Finding the right balance between thorough testing and meeting deadlines
5. **Impact of Quality**: Poor quality directly impacts user satisfaction and business outcomes

---

## 📝 How to Use This Repository

### For QA Testers:
1. Review the test scenarios in `01_Test-Scenarios/`
2. Execute detailed test cases from `02_Test-Cases/` and `03_Negative-Test-Cases/`
3. Document any bugs found in `04_Bug-Reports/` following the existing template
4. Update test cases as new features are added or requirements change

### For Developers:
1. Review test cases before implementing new features
2. Check bug reports to understand reported issues
3. Use test scenarios to verify fixes and new functionality
4. Reference test cases during code reviews

### For Project Managers:
1. Review test documentation to understand testing coverage
2. Track bug reports to monitor quality metrics
3. Use test scenarios for requirement validation
4. Reference known limitations for risk assessment

---

## 🤝 Contributing

When adding new test cases or bug reports:
1. Follow the existing format and structure
2. Use clear, descriptive titles
3. Include all relevant details (steps, expected results, actual results)
4. Add appropriate priority and severity labels
5. Keep documentation updated as requirements evolve

---

## 📧 Contact

For questions or suggestions regarding this QA documentation, please contact the QA team.

---

**Last Updated**: January 2026  
**Repository Owner**: BiyoniMinsandi  
**Project Type**: QA Manual Testing Documentation