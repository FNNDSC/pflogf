# pflogf

[![PyPI version](https://badge.fury.io/py/pflogf.svg)](https://badge.fury.io/py/pflogf)

Colorful logging formatter for fnndsc/pf* family.

pflogf aims to replace [pfmisc/debug.py](https://github.com/FNNDSC/pfmisc/blob/master/pfmisc/debug.py)
using the standard Python [logging](https://docs.python.org/3/library/logging.html) module.

## Examples

```python
import logging
from pflogf import FnndscLogFormatter

logger = logging.getLogger(__name__)
handler = logging.StreamHandler()
handler.setFormatter(FnndscLogFormatter())
logger.addHandler(handler)

logger.setLevel(logging.DEBUG)
logger.debug('debug me as I am full of bugs')
logger.info('an informative statement')
logger.warning('you\'ll probably ignore this warning')
logger.error('error, problem exists between keyboard and chair')
logger.critical('critical failure, haha jk')
```
