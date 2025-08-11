Daily Mobility Analysis: NYU to Columbia Journey
Dataset Description
This GeoJSON dataset captures my daily mobility pattern as a student living near NYU, commuting to Columbia for summer classes, and working in the Robotics Lab. The dataset includes:
Data Types Used:

Points: Specific locations (home, subway stations, coffee cart, lab, etc.)
LineStrings: Movement routes (commute paths, walking routes)
Polygons: Activity areas (Columbia campus area)

Key Attributes:

Temporal: typical_time, duration_minutes, frequency_per_week
Behavioral: stress_level, activity, category
Contextual: cost_dollars, weather_dependent, transport_mode

Related Dataset: MTA Subway Real-Time Data
Primary Dataset: MTA Real-Time Subway Data

Source: Metropolitan Transportation Authority (MTA) GTFS-Realtime feeds
Access: Free API with registration
Update Frequency: Real-time (every 30 seconds)

Dataset Contents:

Train positions and delays
Service alerts and disruptions
Station-level arrival predictions
Route-specific performance metrics

Proposed Methodology for Dataset Integration
Research Questions:

How do subway delays affect my daily stress levels and schedule adherence?
What alternative routes could minimize commute uncertainty?
How does real-time transit performance correlate with my productivity patterns?

Integration Workflow:
Personal Mobility Data + MTA Real-Time Data
                ↓
        Temporal Alignment
                ↓
     Spatial Intersection Analysis
                ↓
      Stress Level Correlation
                ↓
    Predictive Route Optimization
Detailed Steps:
1. Data Preprocessing

Temporal Matching: Align my commute times with MTA service data
Spatial Buffering: Create 200m buffers around my subway stations
Route Mapping: Match my journey with MTA route segments

2. Feature Engineering
python# Pseudocode for key calculations
delay_impact = calculate_delay_impact(
    my_departure_time,
    mta_service_alerts,
    historical_delays
)

stress_correlation = correlate(
    my_stress_levels,
    subway_delays,
    crowding_data
)
3. Analysis Methods
Spatial Analysis:

Buffer analysis around subway stations
Route deviation analysis during service disruptions
Alternative pathway identification

Temporal Analysis:

Commute time variability assessment
Peak hour impact quantification
Seasonal pattern recognition

Behavioral Analysis:

Stress level modeling based on transit conditions
Activity timing adjustment patterns
Location choice optimization

4. Visualization Strategy
Interactive Dashboard Components:

Real-time commute status overlay
Historical delay pattern heatmaps
Stress level correlation charts
Alternative route suggestions

Technical Implementation
Data Fusion Process:

Stream Processing: Real-time MTA data ingestion
Spatial Joins: GIS-based location matching
Time Series Analysis: Pattern detection and forecasting
Machine Learning: Predictive modeling for optimal routing

Tools and Technologies:

GIS Processing: PostGIS, QGIS
Real-time Processing: Apache Kafka, Python
Analysis: pandas, geopandas, scikit-learn
Visualization: Leaflet, D3.js, Plotly

Expected Insights
Quantitative Outcomes:

Average delay impact on commute time
Correlation coefficient between delays and stress
Optimal departure time recommendations
Cost-benefit analysis of alternative routes

Qualitative Outcomes:

Understanding of personal resilience to transit disruptions
Identification of critical decision points in daily routine
Insights into urban mobility adaptation strategies

Limitations and Considerations
Data Quality Issues:

MTA data accuracy during service disruptions
Personal stress level subjectivity
Missing data during system outages

Privacy Concerns:

Location data sensitivity
Temporal pattern exposure
Need for data anonymization in sharing

Methodological Constraints:

Limited sample size (single person)
Seasonal variation coverage
External factor influence (weather, events)

Future Extensions
Additional Related Datasets:

Weather data for correlation analysis
Campus event schedules for context
Citibike availability data for alternative transport
Real-time crowding data from MTA
Google Maps traffic data for surface route comparison

Advanced Analytics:

Machine learning for personalized route prediction
Network analysis for systemic transit vulnerability
Time geography modeling for activity space optimization

This methodology provides a framework for understanding how real-time urban infrastructure performance affects individual daily patterns and decision-making processes.
