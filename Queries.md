TABLE file.link AS "Item", priority, cost-est

FROM "Wishlist-Items" OR "Wishlist-Containers" OR "Wishlist-Locations" OR "Projects"

WHERE status = "planned" OR contains(type, "wishlist")

SORT priority DESC

