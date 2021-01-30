# wurst-unit-status
Wurst API for managing status effects.

## Overview

This library manages an API for attaching a status to a given unit. At its most general, a status is simply some state managed for some unit. Within standard Warcraft III, a status is typically represented by a buff on a unit and the ability responsible for imparting that buff handles the actual effect, such as healing over time, movement speed modification, etc.

This library is focused on the following:
1. Handle imparting a status programmatically as possible, which can be represented by a buff using a dummy ability based on Tornado Slow Aura.
2. Manage the lifetime of a status automatically, including destruction upon unit death, periodic callbacks, and the possibility of being purged or otherwise removed early.

