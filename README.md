# python-learning
Learning Copilot for stock project.
 all_data = get_hk_top_movers_realtime(top_n=len(HK_CORE_POOL))
    if not all_data:
        return []

    from collections import defaultdict
    sector_agg = defaultdict(list)
    for item in all_data:
        sector_agg[item['sector']].append(item)

    summary = []
    for sector, items in sector_agg.items():
