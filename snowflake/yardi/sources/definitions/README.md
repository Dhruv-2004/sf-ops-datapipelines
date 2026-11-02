Definitions are generated in Phase 2, not hand-written.

    python ../../../../../tools/generate_dcm_from_schema.py \
        --env DEV --schema <ZONE>.<SCHEMA> ... \
        --out . --project-name OPS_YARDI

The live account is the source of truth, not changelog.xml. The adoption test is that
PLAN against the generated definitions comes back EMPTY - that is what proves the
migration is mechanical. Any ALTER in that first plan is pre-existing drift between
the changelog and reality, and is a finding worth reporting on its own.
