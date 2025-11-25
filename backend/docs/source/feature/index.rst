Features
================================================================

Overview
--------

This section documents the features in the California Accountability Panel application,
organized as Features (F1-F8) and following an  Agile-ish development methodology.
The 8 Features represents measures of student performance that are annually collected 
across the state and apply to all districts, schools, and student groups. 
Our Feature's architecture is influenced by educational best practices from 
Universal Design for Learning (UDL) by the California Collaborative for Educational Excellence (CCEE), 
from the Testing and Accountability  documentation from the California Department of Education (CDE),
from The College and Career Readiness Evaluation Consortium (CCREC) "Guidelines for GEARUP Program Services" 
and other leading educational organizations. 

Specifically we focus on the predicting 8 of the state and local measures that affect school funding,
in the form of the Local Control Funding Formula (LCFF) and Local Control and Accountability Plans (LCAP).
Throughout the documentation, we highlight how each measure is calculated, displayed, and how it 
aligns with educational goals and supports learning outcomes for K-12 students.


Feature Roadmap
---------------

To gain a general knowledge  of how we define, calculate, and understand what a state measure is, go to http://localhost:8001/feature/e1/


If you would like to know more about a specific state measure/peformance indicator select from the list below:

.. list-table:: Feature Development Status
   :header-rows: 2
   :widths: 10 30 15 45

   * - Feature
     - Name
     - Status
     - Learning Focus
   * - F1
     - ELA Academic Performance Dashboard
     - Planned
     - Scale score trends, performance levels, longitudinal cohort analysis
   * - F2
     - Mathematics Academic Performance Dashboard
     - Planned
     - Data normalization, performance band visualization
   * - F3
     - Science (CAST) Academic Performance
     - Planned
     - Multi-grade aggregation, multi-year trend analysis
   * - F4
     - English Learner Progress (ELPAC)
     - Planned
     - Proficiency level growth, reclassification logic
   * - F5
     - Chronic Absenteeism Tracking
     - Planned
     - Time-series analysis, risk indicators, early warning algorithms
   * - F8
     - Suspension Rate Explorer
     - Planned
     - Ratio calculations, subgroup disparity detection
   * - F7
     - Graduation Rate Dashboard
     - In Progress
     - Cohort models (4-, 5-, 6-year), statistical rate calculations
   * - F8
     - A-G Completion and College/Career Readiness
     - Planned
     - Multi-metric aggregation, readiness scoring engine

Key Architectural Highlights
_____

- **Component-Based Design**: Reusable UI components with clear separation of concerns
- **Data-Driven Development**: Features directly map to California Department of Education (CDE) accountability metrics
- **Accessibility-First**: WCAG 2.1 AA compliance ensures equitable access for all users
- **Privacy by Design**: FERPA-compliant data suppression rules protect student identities

Architecture Principles
-----------------------

**1. Separation of Concerns**

Each Feature (F1-F8) is further implemented using components. This two-tier hierarchy ensures:

- **Maintainability**: Changes to one component don't cascade across the system
- **Testability**: Each layer can be unit tested independently
- **Scalability**: New features can be added without refactoring existing code
- **Reusability**: Components are shared across multiple features

**2. Domain-Driven Design**

Features map directly to educational accountability domains:

- Academic Performance (English Language Arts, Mathematics, Science)
- Student Support (English Learner Progress, Chronic Absenteeism)
- School Climate (Suspension Rates)
- College & Career Readiness (Graduation Rates, A-G Completion)

This alignment ensures the codebase mirrors the mental model of our primary users: educators, administrators, and policymakers.

**3. Progressive Enhancement**

Features are built with a "progressive enhancement" approach:

- **Base Layer**: Semantic HTML providing core functionality
- **Enhancement Layer**: CSS for visual presentation and responsive design  
- **Interaction Layer**: JavaScript for dynamic features (sorting, filtering, trend charts)

This ensures accessibility for users with varying device capabilities and assistive technologies.


Technical Stack (Learning Opportunities)
-----------------------------------------

**Frontend:**

- **React 18+**: Component lifecycle, hooks, state management, virtual DOM
- **TypeScript**: Type safety, interfaces, generics
- **Tailwind CSS**: Utility-first CSS, responsive design, component composition
- **Accessibility**: ARIA roles, keyboard navigation, screen reader compatibility

**Backend:**

- **Python 3.13+**: Modern Python features, type hints, async/await
- **FastAPI**: REST API design, dependency injection, automatic API documentation
- **SQLAlchemy**: ORM patterns, database migrations, query optimization
- **Pydantic**: Data validation, serialization, API schemas

**DevOps & Tooling:**

- **Docker**: Containerization, microservices architecture
- **Git/GitHub**: Version control, pull requests, code review process
- **Sphinx**: Documentation-as-code, reStructuredText markup
- **pytest**: Test-driven development, fixtures, mocking

**Data Processing:**

- **Pandas**: Data manipulation, cleaning, aggregation
- **NumPy**: Statistical calculations, array operations
- **CSV/JSON**: Data format transformation and validation


Contributing to Features
-------------------------

Students and developers can contribute by:

1. **Documentation Improvements**: Fix typos, add examples, clarify technical concepts
2. **Bug Fixes**: Address issues in the GitHub issue tracker
3. **Feature Enhancements**: Propose and implement new accountability metrics
4. **Test Coverage**: Write unit and integration tests to improve code quality
5. **Accessibility Audits**: Test with screen readers and keyboard navigation
6. **Internationalization**: Add support for Spanish language for California's multilingual families

See the :doc:`/developer-guide/index` for detailed contribution guidelines.

Related Documentation
---------------------

- :doc:`/developer-guide/index` - Technical setup and contribution guide
- :doc:`/user-guide/index` - End-user documentation for educators and administrators  
- :doc:`/user-story/index` - User stories and acceptance criteria

External Resources
------------------

**California Education Policy:**

- `California School Dashboard <https://www.caschooldashboard.org/>`_ - Official state accountability system
- `Local Control Funding Formula (LCFF) <https://www.cde.ca.gov/fg/aa/lc/>`_ - Funding and accountability framework
- `LCAP Resources <https://www.cde.ca.gov/re/lc/>`_ - Local Control and Accountability Plans

**Technical Standards:**

- `WCAG 2.1 Guidelines <https://www.w3.org/WAI/WCAG21/quickref/>`_ - Web accessibility standards
- `FERPA Guidance <https://www2.ed.gov/policy/gen/guid/fpco/ferpa/index.html>`_ - Student privacy regulations
- `React Documentation <https://react.dev/>`_ - Frontend framework reference
- `FastAPI Documentation <https://fastapi.tiangolo.com/>`_ - Backend framework reference

**Educational Technology:**

- `Code.org <https://code.org/>`_ - K-12 computer science curriculum resources
- `CS for All <https://www.csforall.org/>`_ - Equity in computer science education
- `ISTE Standards <https://www.iste.org/standards>`_ - Educational technology standards
