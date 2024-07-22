# Monitoring Project with Prometheus and Grafana

This project sets up a monitoring system using Prometheus and Grafana to monitor a sample application.

## Prerequisites

- Docker
- Docker Compose
- Git

## Installation

1. **Clone the Repository:**

    ```bash
    git clone https://github.com/yourusername/monitoring_project.git
    cd monitoring_project
    ```

2. **Start the Services:**

    ```bash
    docker-compose up -d
    ```

## Configuration

### Prometheus

- Configuration file: `prometheus.yml`
- Accessible at: `http://localhost:9090`

### Grafana

- Accessible at: `http://localhost:3000`
- Default credentials: `admin/admin`
- Add Prometheus as a data source with URL `http://prometheus:9090`

## Exposing Metrics

The application exposes metrics at `/metrics`. These metrics are collected by Prometheus and can be visualized in Grafana.

## Creating Dashboards in Grafana

1. **Log In:**
    - Navigate to `http://localhost:3000`
    - Log in using the default credentials: `admin/admin`

2. **Add Prometheus Data Source:**
    - Go to **Configuration** > **Data Sources**
    - Click **Add data source**
    - Select **Prometheus**
    - Set the URL to `http://prometheus:9090`
    - Click **Save & Test**

3. **Create a Dashboard:**
    - Go to **Dashboards** > **Manage**
    - Click **New Dashboard**
    - Add a new panel
    - In the **Query** section, select **Prometheus** as the data source
    - Enter a query like `up` to display the status of the targets
    - Configure the visualization type (e.g., time series)
    - Click **Apply** to save the panel configuration
    - Click the **Save** icon at the top to save the dashboard

## Example Metrics

- **Up Status of Targets:** `up`
- **Prometheus Scrape Duration:** `scrape_duration_seconds`

## License

This project is licensed under the MIT License.
# Monitoring-Project
