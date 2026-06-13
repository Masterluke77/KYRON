# KYRON DATA MODEL

## 1. Grundsatz

PostgreSQL ist die zentrale Datenbank.

Relationaler Kern, JSONB nur für flexible Zusatzdaten.

## 2. Core Tables

Pflichttabellen:

```text
sports
competition_streams
sport_streams
countries
organizations
competitions
seasons
stages
groups
venues
events
event_participants
event_results
event_statistics
participants
participant_memberships
participant_aliases
participant_external_ids
```

## 3. Prediction Tables

```text
prediction_targets
model_families
model_versions
feature_sets
data_snapshots
predictions
prediction_components
prediction_change_log
```

## 4. Rating Tables

```text
rating_universes
participant_ratings
rating_history
```

## 5. Simulation Tables

```text
simulation_runs
simulation_results
```

## 6. Scouting Tables

```text
scouting_universes
scouting_profiles
scouting_metric_values
league_strength_ratings
participant_season_stats
participant_event_stats
shortlists
shortlist_items
scouting_reports
participant_similarity
```

## 7. Data Hub Tables

```text
data_sources
data_source_coverage
data_import_jobs
data_import_errors
data_quality_checks
data_quality_results
```

## 8. User Tables

```text
users
roles
permissions
user_roles
role_permissions
user_preferences
user_picks
user_groups
user_group_members
user_group_leaderboards
watchlists
watchlist_items
notifications
notification_preferences
```

## 9. Audit/Ops Tables

```text
audit_logs
system_logs
jobs
backup_runs
stored_files
```

## 10. Accuracy/Model Lab Tables

```text
model_metrics
prediction_evaluations
calibration_bins
model_drift_checks
backtest_runs
```

## 11. Reports Tables

```text
reports
report_exports
```

## 12. Ads/Consent Tables

```text
sponsors
ad_campaigns
ad_placements
ad_creatives
ad_impressions
ad_clicks
sponsor_contracts
consent_records
privacy_settings
```

## 13. Theme/i18n Tables

```text
themes
theme_tokens
localized_strings
locale_settings
user_interface_preferences
saved_filters
dashboard_layouts
report_templates
report_theme_assignments
```

## 14. Critical Constraints

- `events` must have sport_id and stream_id
- `participants` must have sport_id and stream_id
- event_participants must not mix wrong sport/stream unless explicitly allowed
- predictions require model_version_id and data_snapshot_id
- predictions are append-only
- only one active model per sport/stream/target/family
- ratings must match rating universe
- scouting profiles must match scouting universe
- user picks lock after event start
- ads cannot influence predictions

## 15. Index Strategy

Important indexes:

```text
events(sport_id, stream_id)
events(competition_id, season_id)
events(start_time)
events(status)
participants(sport_id, stream_id)
predictions(event_id, prediction_target_id, predicted_at)
model_versions(sport_id, stream_id, prediction_target_id, model_family_id)
audit_logs(entity_type, entity_id)
user_picks(user_id, event_id)
ad_impressions(campaign_id, created_at)
```
