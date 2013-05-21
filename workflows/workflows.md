# Scenarios

A  the CHW/Clinician submits a monthly report that is validated by Commtrack then forwarded to OpenLMIS.  This triggers creation of an R&R within OpenLMIS; OpenLMIS then generates an Order to be sent to the Supply Point to restock the CHW/Clinician.  Either CommTrack or OpenLMIS (or both) could be the locus of any human review/approval of this replenishment cycle.
 
B  the replenishment process for individual Clinicians/CHWs is handled completely within CommTrack.  OpenLMIS knows there are CHWs operating under the auspices of the Health Center, but does not have any direct interactions with these individuals.  Instead, it sees only the total consumption for the Health Center plus all supported CHWs/Clinicians, as aggregated by CommTrack and reported to OpenLMIS at the end of the month.  OpenLMIS then restocks the Health Center as part of its conventional replenishment process.  Our expectation is that the Requisitions for such a Health Center will be more weighty than those for individual Clinicians/CHWs (both in terms of breadth of commodities and total quantities ordered) and thus follow the conventional process where any human review/approval of the R&R is handled within OpenLMIS
 
# Workflow

1)  the Report is validated by CommTrack, then passed to openLMIS.  OpenLMIS synthesizes a Requisition, which then follows its conventional review-and-approval process, handled by some staff member that has access to OpenLMIS (this could be at the warehouse level or at the HC level, or anywhere in the MoH organizational hierarchy), whereupon it gets released as an Order to be filled by the designated Supply Point.

3)  the Report is validated by CommTrack, then passed to openLMIS.  OpenLMIS synthesizes a Requisition.   Summary details (SOH and Calculated Order Quantity, at least) are passed back to CommTrack.  The HCIC can then review/adjust and approve the Requisition, which is then passed back to OpenLMIS.   The assumptions in this workflow are that (a) the HCIC does not have OpenLMIS access, and instead uses CommTrack to perform their review and approval.   (b) the HCIC can adjust Approved Order Quantities for this Requisition, as they deem appropriate; once reviewed and finalized by this HCIC, this becomes an Approved Requisition which is pushed back to OpenLMIS, where it may or may not undergo further review and approval before being released as an Order.  