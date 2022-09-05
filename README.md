# Pimcore Recycle bin cleanup

When elements get deleted in Pimcore admin area, those elements will get added to the recycle bin. By default Pimcore does not support to automatically remove / purge elements from recycle bin but those stay there forever or until they get deleted manually. This can waste a significant amount of disk space. With this bundle you can define a time threshold after which recycle bin items get deleted automatically.

## Configuration

By default elements older than 30 days get automatically deleted from the recycle bin. You can change this with the config `blackbit_recyclebin_cleanup.storage_threshold` in your /config/config.yaml (for Pimcore >= 10) or `app/config/config.yml` (for Pimcore < 10), e.g.
```yaml
blackbit_recyclebin_cleanup:
  storage_threshold: 60
```