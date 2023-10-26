# 🔐 Security and Audits

Spark upholds the highest security standards, inheriting MakerDAO's security practices and partnering with projects that share the same values.

MakerDAO's security practices & audit reports. [Link to Maker's audits](https://security.makerdao.com/)

## Ethereum Mainnet SparkLend History

SparkLend is based on the Aave V3 codebase which has been extensively audited. [Link to Aave v3's audits](https://docs.aave.com/developers/deployed-contracts/security-and-audits)

SparkLend uses a smaller set of assets than Aave V3 mainnet with similar risk parameters. Extra care is taken to ensure this parity is as close as possible to ensure the attack surface is the same for both markets.

### March 7th, 2023 - Deployment

SparkLend was deployed using the Aave V3.0.1 release using Aave V3 on mainnet as a reference. Notable code differences include:

 * The DAI market has a custom interest rate strategy due to its unique relation with Maker.
 * A custom oracle had to be made for the Savings DAI market.
 * The `RewardsController` was not set up through the `PoolAddressProvider`.
 * The USDC market was added, but not enabled so it used a static $1 as the price oracle.

### April 24-26th, 2023 - Completion of Audits

ChainSecurity completed the audits for the deployment of SparkLend along with audits of the additional code used for the custom interest rate strategy for the DAI market and the Savings DAI oracle.

You can read the full audit reports:

{% file src="../.gitbook/assets/Chainsecurity - SparkLend Deployment Verification" %}

{% file src="../.gitbook/assets/Chainsecurity - DAI IR Strategy and sDAI Oracle" %}

### May 10th, 2023 - SparkLend Launch

Maker activates the D3M in [this spell](https://etherscan.io/address/0x77107F74bf30250aFFada0fbD09fa517658B4916#code) which signals the launch of SparkLend.

### August 20th, 2023 - Upgrade to Aave V3.0.2

An [upgrade is performed](https://etherscan.io/address/0x60cc45dab5f0b17789c77d5fe990f1ad80e9dd65#code) from V3.0.1 to V3.0.2 to bring the code in line with the latest changes from the Aave codebase to patch a few minor issues.

### October 19th, 2023 - USDC Market Enabled

USDC market is enabled and the $1 fixed price oracle is replaced with a real one. This update also enabled a USD e-mode which does not exist on Aave V3 as of the time of this writing.

## Savings DAI Audit (sDAI)

{% file src="../.gitbook/assets/Chainsecurity - sDAI" %}
