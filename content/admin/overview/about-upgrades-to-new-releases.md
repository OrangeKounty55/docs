
Web page not available
The web page at https://clickout.sharethrough.com/?clickout_url=https%3A%2F%2Fprod-use.perf-serving.com%2Fclick%2FlN0JR8ZncIgTIQRIDCA8_lvoQsY4tnbS1UrbkqVuNu0KhtZZR6vfKIyYquAiMKeddfX6YuDRipVQdCH8CXiOMklKTysAdj9oz9xqHMU_kf_MbW1gQa885x052BsFi6td4ytMa5-rVSTltt1qvGSwGqrOClKpeuajorkZ3tD9Ub97gSBZjVhP__UF3NU_Bm-DTlXyASncPXULmYYXndDdnZYyD27ZK2cVTvdhxICDerMuORaZPwyZcfKFkiHENfdGfhHtHcd23zdjcpJdc1TqT-OvRHyi7YyZP9AO9ZYZdihwPlToRDX4sTIj7kjGha3VUnZRvF23I0DNlwKQ2T7UC94wS_WAqivBbgQRNsuCe8ZmBmGcC1QiT9cGiN8trPmU8xWD1cPm9LTiRQDLN4HW8U3dyMZ080bVZH9m4_mltSsBsCjHRWzI3m4B5XzkZmFQM1T6tnEBejIfWSKxdImxM5UzX1x8ZO8HbwHue712Ubh8PLPkoIek3w6sXgoY11anehPE7JhezuV6eHeyIkNNKrQOqG9Lb8L0o6LdgKjzowa2OJ_DzF7DJYK836opr_fY0-AXye_52-S7X9v-bdJQTovM75Ybq_9OvQSVAmOnCX3lDCPUhO16KTX8FKYCsjwJhzKK6n7gZxlEygFqHsZfYXGTpVE_FOtxOUA93uv_pYbGp0tq02i_qXtQz4njrTfJHx_EPoJkG-gsYjvwBbfgaa02F3yUlwng095yUA9FKvYAJp29dy4LteFrWiU-N_Mb1KI51pJzIsgPxCAvz8RSB6c3TqyKds38hJrB7X_87WVJBzKNc4fsoGTFY6oknag4W3aNBWc5JU3hUlR_R8owStd5-W6CNEOHRqSaocHHH_gOFR9CKBws5r0a8fbmftlCyEeNWXWIgs8_Cd5IMQ_jwLgc0TKINPQ9iX6En3sWo_Lm0whn1r67ktg334SmbxkoJgq5L6G50YBVqdFMwQsnhDI8lzji9a_nbRDpAnOrthf_wI20wqZ1qnvKCLwun9u4uNiUgcJLv3nI4IzIrjP8NT1shS8awWz3EkEiu0xZtXwIDyp-uH6IP4YtbIPoCMitFX6APCB4sI3ZMmJ0g7CkQwy5CHi8TWD0v-n_TilTv4wK4Q7mQcuQeO2WtSywxbvxjFaxFDsfEVPIBbTB9WjMjOCIO7Z1pF2-AlBrONQO27eLvQ8lw2SMg7yz3t8EfUXMH4zP13YoUSqxkEC1vrrGxcYvUDvxqpLz%2F%2F%2F&token=47685db65eb05ec7ed99915103949647d4287b1c&nonce=2832855bf7b25a8165fd8459180d656ebf6bf96b could not be loaded because:

net::ERR_CONNECTION_CLOSED

---
title: About upgrades to new releases
shortTitle: About upgrades
intro: '{% ifversion ghae %}Your enterprise on {% data variables.product.product_name %} is updated with the latest features and bug fixes on a regular basis by {% data variables.product.company_short %}.{% else %}You can benefit from new features and bug fixes for {% data variables.product.product_name %} by upgrading your enterprise to a newly released version.{% endif %}'
versions:
  ghes: '*'
  ghae: '*'
type: overview
topics:
  - Enterprise
  - Upgrades
---
{% ifversion ghes < 3.3 %}{% data reusables.enterprise.upgrade-ghes-for-features %}{% endif %}

{% data reusables.enterprise.constantly-improving %}{% ifversion ghae %}{% data variables.product.prodname_ghe_managed %} is a fully managed service, so {% data variables.product.company_short %} completes the upgrade process for your enterprise.{% endif %}

Feature releases include new functionality and feature upgrades and typically occur quarterly. {% ifversion ghae %}{% data variables.product.company_short %} will upgrade your enterprise to the latest feature release. You will be given advance notice of any planned downtime for your enterprise.{% endif %}

{% ifversion ghes %}

Starting with {% data variables.product.prodname_ghe_server %} 3.0, all feature releases begin with at least one release candidate. Release candidates are proposed feature releases, with a complete feature set. There may be bugs or issues in a release candidate which can only be found through feedback from customers actually using {% data variables.product.product_name %}. 

You can get early access to the latest features by testing a release candidate as soon as the release candidate is available. You can upgrade to a release candidate from a supported version and can upgrade from the release candidate to later versions when released. You should upgrade any environment running a release candidate as soon as the release is generally available. For more information, see "[Upgrade requirements](/admin/enterprise-management/upgrade-requirements)."

Release candidates should be deployed on test or staging environments. As you test a release candidate, please provide feedback by contacting support. For more information, see "[Working with {% data variables.contact.github_support %}](/admin/enterprise-support)."

We'll use your feedback to apply bug fixes and any other necessary changes to create a stable production release. Each new release candidate adds bug fixes for issues found in prior versions. When the release is ready for widespread adoption, {% data variables.product.company_short %} publishes a stable production release.

{% endif %}

{% warning %}

**Warning**: The upgrade to a new feature release will cause a few hours of downtime, during which none of your users will be able to use the enterprise. You can inform your users about downtime by publishing a global announcement banner, using your enterprise settings or the REST API. For more information, see "[Customizing user messages on your instance](/admin/user-management/customizing-user-messages-on-your-instance#creating-a-global-announcement-banner)" and "[{% data variables.product.prodname_enterprise %} administration](/rest/reference/enterprise-admin#announcements)."

{% endwarning %}

{% ifversion ghes %}

Patch releases, which consist of hot patches and bug fixes only, happen more frequently. Patch releases are generally available when first released, with no release candidates. Upgrading to a patch release typically requires less than five minutes of downtime.

To upgrade your enterprise to a new release, see "[Release notes](/enterprise-server/admin/release-notes)" and "[Upgrading {% data variables.product.prodname_ghe_server %}](/admin/enterprise-management/upgrading-github-enterprise-server)." Because you can only upgrade from a feature release that's at most two releases behind, use the [{% data variables.enterprise.upgrade_assistant %}](https://support.github.com/enterprise/server-upgrade) to find the upgrade path from your current release version.

{% endif %}

## Further reading

- [ {% data variables.product.prodname_roadmap %} ]( {% data variables.product.prodname_roadmap_link %} ) in the  `github/roadmap` repository{% ifversion ghae %}
- [ {% data variables.product.prodname_ghe_managed %} release notes](/admin/release-notes)
{% endif %}
