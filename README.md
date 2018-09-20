# BULVRD.IPFS.Rewards
Repo for documentation related to BULVRD in-app rewards granted to users based on contributions made

## The Spec
BULVRD app(s) will post in-app rewards granted to users as contributions are made to the ecosystem. On the mission for transparency, these rewards are posted to IPFS to allow for community and user auditing. The reward scale is currently outlined in our whitepaper and will also be baked into the Smart Contract. We may find needs to revamp this scale over time and will be versioned against the BULVRD Smart Contract as needed. BULVRD infrastructure will make all attempts to keep this feed as real time as possible, but please note that if a user/device is in a low to no network connection area/state, there will be a delay in this data being posted.

Data will be posted directly to IPFS in json format. BULVRD will run it's own IPFS node and pin all validated data. The data sets will be structured with the following values:
- reward : Integer - Reward granted to user
- reason : String - String value for reason reward was given
- addy : String - Wallet address of receiver of reward 
- contractAddy : String - Address of reference Smart Contract
- timestamp : Long - Millisecond timestamp of reward grant

For a working example:
`
{
"reward" : 3,
"reason" : "Traffic",
"addy" : "0x123456",
"contractAddy" : "0x123456",
"timestamp" : 1534640601,
}
`
