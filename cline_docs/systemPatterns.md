# System Patterns

## Architecture
The system follows a modular architecture with clear separation of concerns:

### Core Components
1. CrawlSession (session.py)
   - Orchestrates the crawling process
   - Manages resources and connectors
   - Validates crawl paths

2. Crawler (crawler.py)
   - Handles HTTP requests
   - Implements retry logic
   - Manages pagination
   - Currently implements SimpleRequestsCrawler

3. Connector (connector.py)
   - Handles data storage
   - Supports filesystem and MongoDB

4. Document (document.py)
   - Represents crawled content
   - Handles document formatting

### Key Technical Decisions
1. Modular Design
   - Abstract base classes for extensibility
   - Pluggable components (crawlers, connectors)
   - Clear interfaces between components

2. Configuration
   - Resource validation
   - Configurable headers
   - Adjustable retry policies

3. Error Handling
   - Automatic retries with standoff
   - Timeout handling
   - Response validation

## Design Patterns
1. Strategy Pattern
   - Different crawler implementations
   - Multiple connector types

2. Factory Pattern
   - DefaultCrawlSession creation
   - Document creation

3. Dependency Injection
   - Crawler and connector injection into sessions