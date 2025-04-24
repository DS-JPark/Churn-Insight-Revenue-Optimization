## Churn Insight & Revenue Optimization

# Project goal #: To identify churn risk among users of a subscription-based fintech app and propose data-driven marketing strategies to improve retention and increase lifetime value.

This is a project combining e-commerce, marketing, and fintech.

### Data Model
The database contains the following entities in a star schema.
1. Customers:
    * customer_id (PK)
    * signup_date
    * age
    * gender
    * region
    * device_type
    * acquisition_channel

2. Subscription Events
    * customer_id (FK)
    * start_date
    * end_date
    * plan_type
    * is_active
    * churn_flag
    * churn_reason

3. Transactions
    * transaction_id (PK)
    * customer_id (FK)
    * transaction_date
    * amount_in_euro
    * payment_method

4. Marketing Campaigns
    * campaign_id (PK)
    * customer_id (FK)
    * channel
    * open_rate
    * click_through_rate
    * conversion

5. Engagement Logs
    * customer_id (FK)
    * login_time
    * action_type
    * session_duration