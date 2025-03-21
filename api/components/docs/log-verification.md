### [Draft]Test Scenarios WO - 2.0

Logs to be submitted for applicable flows below by creating PR on the following [GitHub Repository](https://github.com/ONDC-Official/ONEST-LOGS-VERIFICATION).

---
### Flow Details

- **Flow 1: Catalog Pull and Refresh**
1. Seeker NP initiates full catalog pull → search
1. Provider responds with full catalog → on_search
1. Seeker NP initiates catalog incremental refresh request → search
1. Provider NP responds with incremental catalog refresh response → on_search

- **Flow 2: Application and Offer Acceptance**
1. Seeker NP initiates full catalog pull → search
1. Provider responds with full catalog → on_search
1. Seeker selects one application for applying → select
1. Provider NP provides all fulfillment slots and different fulfillment types → on_select
1. Seeker selects the fulfillment and provides its information → init
1. Provider requests additional information related to seeker using forms. → on_init
1. The provider acknowledges that all forms are filled → on_init  (unsolicited)
1. Seeker confirms the application → confirm
1. Provider accepts or submits the application → on_confirm
1. Provider accepts the application → on_status (unsolicited) (only required if on_confirm has APPLICATION_SUBMITTED fulfillment status.) 
1. Provider performs assessment related to the application → on_status (unsolicited)
1. The provider extends the offer to the seeker and updates the fulfillment → on_update (unsolicited) OR on_status (unsolicited) (if offer letter is included, the call must be on_update, otherwise it must be on_status) 
1. Seeker accepts the offer → update
1. Provider acknowledges the offer acceptance → on_update

- **Flow 3: Application Rejection**
1. Seeker NP initiates full catalog pull → search
1. Provider responds with full catalog → on_search
1. Seeker selects one application for applying → select
1. Provider NP provides all fulfillment slots and different fulfillment types → on_select
1. Seeker selects the fulfillment and provides its information → init
1. Provider requests additional information related to seeker using forms. → on_init
1. The provider acknowledges that all forms are filled → on_init (unsolicited)
1. Seeker confirms the application → confirm
1. Provider confirms the application → on_confirm
1. Provider rejects the application → on_status (unsolicited)

---


For detailed flow steps and further assistance, please refer to the [official documentation](https://docs.google.com/spreadsheets/d/118ShHWOE5Lx3Wh_35VLadqltMjp_AkCIZW0prP9xbNY/edit?gid=0#gid=0).

