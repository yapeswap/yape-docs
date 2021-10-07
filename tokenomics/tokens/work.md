# Work

Work is where the $cYAPE magic happens. Work is powered by:

1. Projects on the 📋 **Project Board**
2. The 🔄 **Stable Reserve Redemption System**

## 📋 Project Board <a id="project-board"></a>

* **Anyone** can post a project on the Project Board.
* **Budget Owner/Admins** are the ones who create and post projects.

1. Projects are **funded** with **$cYAPE** tokens as contributions.
2. A project's Budget Owner can pay contributors at once or stream payments over time.
3. \(Optional\) Projects can also choose to start an **Initial Contributor Sharing Program \(ISCP\)**

{% tabs %}
{% tab title="Funding" %}
Budget owners/admins are not the only people who can fund a project--theoretically **anyone** can join in on the cause and contribute to a project's payout funding. That being said, there is no mechanism enforcing a budget owner/admin to keep track of, record, or honor any of a project's additional financial contributions beyond his/her own.
{% endtab %}

{% tab title="$cYAPE" %}
Any contribution \(with $cYAPE\) to a project is automatically recorded as a contribution. **Recorded contributions are valuable because they count toward emission shares when the project later upgrades to a DAO.**
{% endtab %}

{% tab title="Initial Contributor Sharing Program" %}
1. All financial and work contributions are recorded. These recorded contributions guarantees a percentage of the token emission to a project's initial contributors when the project upgrades to a DAO.
2. Only the Budget Owner has access to Admin functions. The Budget Owner can setup the ICSP, transfer ownership to a multisig wallet, and record contributions.
   1. All projects on WHF initially start with a single Ethereum account as the Budget Owner.
   2. The project owner\(s\) may choose to transfer and decentralize ownership to a Gnosis multisig wallet.
{% endtab %}
{% endtabs %}

## 🔄 Stable Reserve <a id="stable-reserve"></a>

Work is straightforward: get paid in $cYAPE or don't work and instead buy $cYAPE. The Stable Reserve is the only contract that can mint $cYAPE.

**1$cYAPE → StableReserve → 1$DAI**

**2$DAI → StableReserve → 1$cYAPE**

{% tabs %}
{% tab title="Price Floor" %}
Because the circulating supply of $cYAPE will always be less than $DAI in the Stable Reserve, there is an effective floor of 1 $DAI for 1 $cYAPE and a ceiling of 2 $DAI.
{% endtab %}

{% tab title="Arbitrage" %}
In the rare case that 1 $cYAPE goes over 2 $DAI, any trader can take advantage of this arbitrage opportunity and trade away the difference at Decentralized Exchanges.
{% endtab %}
{% endtabs %}

With your $cYAPE, you can choose to burn $cYAPE to mine $YAPE \(rather than immediately cashing out into $DAI\).

Commit mining and buying $cYAPE at a premium ensures there's extra $cYAPE in the Stable Reserve. If `Reserved $DAI - Circulating $cYAPE = x`, the community can vote to mint x $cYAPEs and grant them to projects. Extra $cYAPE means a larger budget for Yapeswap to pay more contributors. Effectively this mechanism between $cYAPE and $YAPE works like liquid stock options.

