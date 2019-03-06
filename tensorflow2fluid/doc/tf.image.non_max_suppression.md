
## tf.image.non_max_suppression

### [tf.image.non_max_suppression](https://www.tensorflow.org/api_docs/python/tf/image/non_max_suppression)
``` python
tf.image.non_max_suppression(
    boxes,
    scores,
    max_output_size,
    iou_threshold=0.5,
    score_threshold=float('-inf'),
    name=None
)
```

### [paddle.fluid.layers.multiclass_nms](http://paddlepaddle.org/documentation/docs/en/1.3/api/layers.html#permalink-245-multiclass_nms)
``` python
paddle.fluid.layers.multiclass_nms(
    bboxes, 
    scores, 
    score_threshold, 
    nms_top_k, 
    keep_top_k, 
    nms_threshold=0.3, 
    normalized=True, 
    nms_eta=1.0, 
    background_label=0, 
    name=None)
```

### 功能差异：
#### 输入格式：
>  tensorflow：`boxes`的shape为`[num_boxes, 4]`， `scores`的shape为`[num_boxes]`
>  paddlepaddle：支持batch和多类别，`bboxes`的shape为`[batch, num_boxes, 4]`， `scores`的shape为`[batch, num_classes, num_boxes]`

## paddlepaddle示例:
```python

# 常量tensor out 中数据为 np.array([[5,5,5],[5,5,5]], dtype='int64')
out = fluid.layers.fill_constant(shape=[2,3], dtype='int64', value=5)  