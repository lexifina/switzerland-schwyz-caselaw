# Reproducing this repository

Input: the Parquet files listed below, revision `fecc2c971945cacd914c63b54ee22db9149e58c9` of the `voilaj/swiss-caselaw` dataset
(`https://huggingface.co/datasets/voilaj/swiss-caselaw/resolve/fecc2c971945cacd914c63b54ee22db9149e58c9/<file>`), plus `graph/statute_references.parquet`
from the same revision, and lexifina/switzerland-law `main` for the overlay's `law_commit`.

```
python tools/build.py sz <cache with data/ and graph/> <empty folder> --today 2026-11-06
```

Needs Python 3 and `duckdb`. Gives 5,708 decision commits and one documentation commit, hash for hash.

## SHA-256 of the input files

```
aeac829221392dc3df043b458fc3e14a9650e15f84bea6251fbbd9afca15d766 *sz_gerichte.parquet
03ecc36c7161662da4b7b97d120ed7d3d7d53227157e800160b581e482b8b22b *sz_verwaltungsgericht.parquet
```
