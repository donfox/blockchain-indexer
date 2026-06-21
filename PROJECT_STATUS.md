# blockchain_indexer - Project Status

## Status: ✅ PRODUCTION-READY

**Purpose**: Hybrid batch processing blockchain indexer combining best practices

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
