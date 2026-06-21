# blockchain_indexer - Project Status

## Status: ✅ Core Pipeline Complete (Portfolio Ready)

**Purpose**: Demonstrate a hybrid batch-processing blockchain indexer with modular services, observability, and operational safeguards.

## Readiness Notes
- Core collection, processing, and gap-management flow is implemented and documented.
- Operational features (retry logic, metrics, and graceful shutdown) are present.
- Full automated test coverage and deployment automation are planned next steps.

## Architecture
- Batch processing with configurable sizes
- Python multiprocessing (no Redis dependency)
- Dual storage: PostgreSQL + JSON files
- Automatic gap detection and fixing
- Comprehensive metrics and health checks

## Components
- `block_collector.py` - Fetches latest blocks
- `block_processor.py` - Processes and stores blocks
- `gap_detector.py` - Identifies missing blocks
- `gap_fixer.py` - Fixes gaps in block sequences

## Dependencies
requests, psycopg2-binary, tenacity, python-json-logger

## Run Command
```bash
pip install -r requirements.txt
python main.py [--batch-size N] [--workers N] [--skip-gaps]
```
