# Product Context

## Purpose
wordpress-scraper is a tool designed to easily scrape data from WordPress sites using their JSON API. It provides a simple interface for extracting content while handling common challenges in web scraping.

## Problems Solved
1. Automated extraction of WordPress content (posts, categories, tags)
2. Handles pagination and retries automatically
3. Flexible storage options (MongoDB/filesystem)
4. Error handling and retry mechanisms
5. Configurable crawling parameters

## Expected Functionality
- Basic Usage: Simple command-line interface to crawl WordPress sites
- Data Storage: Saves crawled content as JSON files or MongoDB documents
- Error Handling: Automatic retries with configurable policies
- Resource Types: Currently supports posts, categories, and tags
- Customization: Extensible architecture for custom crawling sessions

## Current Limitations
- No authentication support yet
- No Cloudflare bypass
- Limited to basic WP API resources
- Synchronous operation only