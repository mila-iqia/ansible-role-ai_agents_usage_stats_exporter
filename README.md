Slurm Job Exporter
==================

This role installs and configures the Prometheus [AI Agents Usage Stats Exporter](https://github.com/mila-iqia/ai-agents-usage-stats-exporter).

Role Variables
--------------

See [defaults/main.yml](defaults/main.yml).

To use a fork of the default GitHub project:

    # Define git repository
    ai_agents_usage_stats_exporter_git_repo: "https://github.com/mila-iqia/ai-agents-usage-stats-exporter.git"

To install a new release:

    ai_agents_usage_stats_exporter_version: "v0.1.0"

To define an alternate installation path:

    ai_agents_usage_stats_exporter_path: "/path/to/ai-agents-usage-stats-exporter"


Example Playbook
----------------

Install and configure the exporter:

    - hosts: computes
      vars:
        ai_agents_usage_stats_exporter_version: v0.1.0
      tasks:
        - name: Import role mila.ai_agents_usage_stats_exporter
          ansible.builtin.import_role:
            name: mila.ai_agents_usage_stats_exporter
          tags: role::ai_agents_usage_stats_exporter

